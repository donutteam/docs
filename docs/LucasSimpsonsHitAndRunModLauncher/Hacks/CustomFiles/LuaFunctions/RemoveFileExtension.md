---
title: "RemoveFileExtension"
description: "Returns the given file path or file name without the file extension."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 355 # 1.8
---

Returns the given file path or file name without the file extension.

# Syntax
```lua
RemoveFileExtension( path )
```

## Arguments
* **path** (string): The path or filename of the file you want to remove the extension from.

## Return Values
* (string): The given file path or file name without the file extension.

# Examples
```lua
-- Returns "example"
RemoveFileExtension("example.mfk")

-- Returns "scripts\example"
RemoveFileExtension("scripts\\example.mfk")
```