---
title: "File.ReadOffset"
description: "Provides information about the File.ReadOffset function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Reads a portion of a file starting from a specific offset.

# Syntax
```lua
File.ReadOffset( path, offset, length )
```

## Arguments
* **path** (string): The path of the file to read.
* **offset** (number): The position in the file to start reading from.
* **length** (number): The number of bytes to read from the file.

## Return Values
* (string): Returns the content of the file as a string, or nil if the file does not exist.


# Examples
```lua
local content = File.ReadOffset("path/to/the_bee_movie_script.txt", 0, 100)
if content then
    print("File content:", content)
end
```