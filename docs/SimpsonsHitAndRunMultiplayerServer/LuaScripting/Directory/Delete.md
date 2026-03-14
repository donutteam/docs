---
title: "Directory.Delete"
description: "Provides information about the Directory.Delete function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Deletes a directory at the specified path.


# Syntax
```lua
Directory.Delete( path, [ recursive ] );
```

## Arguments
* **path** (string): The path of the directory to delete.
* **recursive** (boolean, optional): If true, deletes the directory and all its contents recursively. Defaults to false.

## Return Values
* (boolean): Returns true if the directory was deleted successfully, or false if an error occurred (e.g., if the directory does not exist or if the path is invalid).


# Examples
```lua
local success = Directory.Delete("new_directory")
if success then
    print("Directory deleted successfully!")
else
    print("Failed to delete directory.")
end
```