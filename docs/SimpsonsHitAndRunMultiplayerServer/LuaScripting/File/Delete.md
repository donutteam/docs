---
title: "File.Delete"
description: "Provides information about the File.Delete function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Deletes a file at the specified path.

# Syntax
```lua
File.Delete( path, content )
```

## Arguments
* **path** (string): The path of the file to delete.

## Return Values
* (boolean): Returns true if the file was deleted successfully, or false if an error occurred (e.g., if the path is invalid).

# Examples
```lua
local result = File.Delete("path/to/file.txt")
if result then
    print("File deleted successfully!")
else
    print("Failed to delete file.")
end
```