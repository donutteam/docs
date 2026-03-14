---
title: "GetFileExtension"
description: "Returns the file extension of the specified path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 355 # 1.8
---

Returns the file extension of the specified path.

# Syntax
```lua
GetFileExtension( path )
```

## Arguments
* **path** (string): The path or filename of the file you want to get the extension of.

## Return Values
* (string): The file extension.

# Examples
```lua
-- Returns ".mfk"
GetFileExtension("example.mfk")
```