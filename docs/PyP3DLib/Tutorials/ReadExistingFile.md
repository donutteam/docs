---
title: "Read an Existing P3D File"
description: "Learn how to read an existing P3D file with PyP3DLib."
authors: [ 2 ]
---

This library can load and read standard or compressed P3D files in little or big endian.

# 1. Import PyP3DLib
Doing so is pretty simple, simply import the `p3d` package:
```py
import p3d
```

# 2. Read a File
And then pass a path (either a `str` or a `pathlib.Path`) to the `p3d.P3DFile` constructor:
```py
file_path = "C:\\Program Files (x86)\\Vivendi Universal Games\\The Simpsons Hit & Run\\art\\L1_TERRA.p3d"

# P3DFile accepts str or pathlib.Path
p3d_file = p3d.P3DFile(file_path)
```

Some possible exceptions raised by reading a P3D file are:
* `FileNotFoundError`: The given `file_path` does not exist.
* `ValueError`:
	* The file's size is smaller than 12 bytes.
	* The file's size is larger than 2,147,483,647 bytes.
	* The file's (decompressed) signature is not valid.
* `EOFError`: Failed to read the file signature.
* `IOError`: Reading a chunk consumed 0 bytes.

# Examples
Once you have read a file, you can then manipulate `p3d_file.chunks` (which is a [list](https://docs.python.org/3/library/stdtypes.html#typesseq-list)-like object) and the chunks within it to modify the file. Below are a couple of examples.

## Count Chunks
Here is an example that iterates all the chunks in a file, counts how many of each type there is, and then prints the counts:
```py
import p3d

file_path = "C:\\Program Files (x86)\\Vivendi Universal Games\\The Simpsons Hit & Run\\art\\missions\\level01\\level.p3d"
p3d_file = p3d.P3DFile(file_path)

chunk_counts: dict[type[p3d.Chunk], int] = {}

for chunk in p3d_file.chunks:
	chunk_counts[type(chunk)] = chunk_counts.get(type(chunk), 0) + 1

for chunk_type, chunk_count in chunk_counts.items():
	print(f"{chunk_type.__name__}: {chunk_count}")

# For the original level01/level.p3d, this should print:
#	TextureChunk: 1
#	ShaderChunk: 1
#	MeshChunk: 1
#	LocatorChunk: 124
```

## Reposition All Locators
Here is another example that will load a file, adjust the positions of all of its [[/Pure3DFiles/ChunkTypes/Locator.md]] chunks, and then write it to a new file:
```py
import p3d
import p3d.chunks

file_path = "C:\\Program Files (x86)\\Vivendi Universal Games\\The Simpsons Hit & Run\\art\\missions\\level01\\level.p3d"
p3d_file = p3d.P3DFile(file_path)

locator_chunks = p3d_file.get_chunks_of_type(p3d.chunks.LocatorChunk)

for locator_chunk in locator_chunks:
	# Move all the locators up by 5 meters, for some reason!
	locator_chunk.position.y += 5.0

new_file_path = "C:\\Path\\To\\new_file.p3d"
p3d_file.write(new_file_path)
```