---
title: "Writing a New P3D File"
description: "Learn how to write a brand new P3D file with PyP3DLib."
authors: [ 2 ]
---

How complex creating and writing a new P3D file with PyP3DLib is depends upon what type of file you're trying to create.

In this tutorial, you will learn how to create a basic file that contains a [[/Pure3DFiles/ChunkTypes/History.md]] chunk and a Generic [[/Pure3DFiles/ChunkTypes/Locator.md]] chunk.

# 1. Import PyP3DLib
For this tutorial, you will need to import:
* `p3d`: The core library with the `P3DFile` class.
* `p3d.chunks`: Where chunk classes live.
* `p3d.math`: Where various math classes, such as `Vector2`, `Vector3` and `Matrix` live.

```py
import p3d
import p3d.chunks
import p3d.math
```

# 2. Create a History Chunk
To create a [[/Pure3DFiles/ChunkTypes/History.md]] chunk, simply call the constructor with `history` (`Iterable[str]`):

```py
history_chunk = p3d.chunks.HistoryChunk(
	history = [
		"Line of text!",
		"Another line of text!",
	],
)
```

# 3. Create a Generic Locator Chunk
To create a Generic [[/Pure3DFiles/ChunkTypes/Locator.md]] chunk, you need to pass in
* `name` (`str`): The name of the locator.
* `type_data` (`LocatorData`): One of the many kinds of `LocatorData` classes.
	* In this case, `GenericLocatorData` which does not take any additional parameters.
* `position` (`Vector3`): The position of the locator.

```py
locator_chunk = p3d.chunks.LocatorChunk(
	name = "my_locator",
	type_data = p3d.chunks.LocatorChunk.GenericLocatorData(),
	position = p3d.math.Vector3(5.0, 5.0, 5.0),
)
```

# 4. Create the File
Now that you have some chunk instances, it is time to put them into a file!

First, construct a `P3DFile` with no parameters:
```py
p3d_file = p3d.P3DFile()
```

That creates a new, empty `P3DFile` you can then add chunks to via the `append` (for single chunks) and `extend` (for multiple chunks) methods on the file's `chunks` (a [list](https://docs.python.org/3/library/stdtypes.html#typesseq-list)-like object).

In this case, you have multiple chunks so you should use `extend`:
```py
p3d_file.chunks.extend([
	history_chunk,
	locator_chunk,
])
```

# 5. Write the File
Now all you need to do is write your file to disk somewhere using the `write_file` method:
```py
file_path = "C:\\Path\\To\\output_file.p3d"
p3d_file.write_file(file_path)
```

# Examples
## Full Example
Here is all the steps above together as a full example script:
```py
import p3d
import p3d.chunks
import p3d.math

history_chunk = p3d.chunks.HistoryChunk(
	history = [
		"Line of text!",
		"Another line of text!",
	],
)

locator_chunk = p3d.chunks.LocatorChunk(
	name = "my_locator",
	type_data = p3d.chunks.LocatorChunk.GenericLocatorData(),
	position = p3d.math.Vector3(5.0, 5.0, 5.0),
)

p3d_file = p3d.P3DFile()

p3d_file.chunks.extend([
	history_chunk,
	locator_chunk,
])

file_path = "C:\\Path\\To\\output_file.p3d"
p3d_file.write_file(file_path)
```

## Chunk Ownership and Cloning
When chunks are added to a file, they become *owned* by that file. This means they cannot be added to any other file's chunks or any other chunk's children without being removed or cloned.

In the case of cloning, simply call the `clone` method available on any `Chunk` class.
```py
# ...continuing from the "Full Example" above...

another_locator_chunk = locator_chunk.clone()
another_locator_chunk.name = "another_locator"
another_locator_chunk.position.x += 5.0

another_p3d_file = p3d.P3DFile()
another_p3d_file.chunks.append(another_locator_chunk)

another_file_path = "C:\\Path\\To\\other_output_file.p3d"
another_p3d_file.write_file(another_file_path)
```