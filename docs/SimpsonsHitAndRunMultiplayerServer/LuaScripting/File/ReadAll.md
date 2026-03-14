---
title: "File.ReadAll"
description: "Provides information about the File.ReadAll function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Reads the entire content of a file.

# Syntax
```lua
File.ReadAll( path )
```

## Arguments
* **path** (string): The path of the file to read.

## Return Values
* (string): Returns the content of the file as a string, or nil if the file does not exist.


# Examples
```lua
local content = File.ReadAll("path/to/the_bee_movie_script.txt")
if content then
    print("File content:", content)
end
```