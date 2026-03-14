---
title: "File.Write"
description: "Provides information about the File.Write function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Writes content to a file at the specified path. If the file already exists, it will be overwritten.

# Syntax
```lua
File.Write( path, content )
```

## Arguments
* **path** (string): The path of the file to write to.
* **content** (string): The content to write to the file.

## Return Values
* (boolean): Returns true if the file was written successfully, or false if an error occurred (e.g., if the path is invalid).

# Examples
```lua
local result = File.Write("path/to/file.txt", "Hello, world!")
if result then
    print("File written successfully!")
else
    print("Failed to write file.")
end
```