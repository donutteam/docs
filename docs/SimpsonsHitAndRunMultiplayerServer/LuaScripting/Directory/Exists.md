---
title: "Directory.Exists"
description: "Provides information about the Directory.Exists function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a directory exists at the specified path.


# Syntax
```lua
Directory.Exists( path );
```

## Arguments
* **path** (string): The path of the directory to check.

## Return Values
* (boolean): Returns true if the directory exists, or false if it does not exist or if the path is invalid.


# Examples
```lua
if Directory.Exists("my_directory") then
    print("Directory exists!")
end
```