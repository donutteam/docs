---
title: "File.Exists"
description: "Provides information about the File.Exists function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a file exists at the specified path.

# Syntax
```lua
File.Exists( path )
```

## Arguments
* **path** (string): The path of the file to check.

## Return Values
* (boolean): Returns true if the file exists, or false if it does not exist.


# Examples
```lua
local exists = File.Exists("path/to/file.txt")
if exists then
    print("File exists!")
end
```