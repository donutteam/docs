---
title: "Directory.Scan"
description: "Provides information about the Directory.Scan function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Scans a directory and returns a table containing the names of all files and subdirectories within it.

# Syntax
```lua
Directory.Scan( path, [pattern] )
```

## Arguments
* **path** (string): The path of the directory to scan. This can be an absolute path or a path relative to the mod's directory.
* **pattern** (string, optional): A pattern to match file names against. Defaults to "*" if not specified.

## Return Values
* (table): A table containing the names of all files and subdirectories within the specified directory. The keys of the table are integers starting from 1, and the values are strings representing the names of the files and subdirectories.


# Examples
```lua
local scannedFiles = Directory.Scan("events", "*.lua")

for i = 1, #scannedFiles do
    File.RequireOnce(scannedFiles[i])
end
```