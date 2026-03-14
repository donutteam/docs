---
title: "Directory.Create"
description: "Provides information about the Directory.Create function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Creates a new directory at the specified path.

# Syntax
```lua
Directory.Create( path )
```

## Arguments
* **path** (string): The path of the directory to create.

## Return Values
* (boolean): Returns true if the directory was created successfully, or false if an error occurred (e.g., if the directory already exists or if the path is invalid).


# Examples
```lua
local success = Directory.Create("new_directory")
if success then
    print("Directory created successfully!")
else
    print("Failed to create directory.")
end
```