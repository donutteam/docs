---
title: "GetFileName"
description: "Returns the file name of the specified path including the extension."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Returns the file name of the specified path including the extension.

# Syntax
```lua
GetFileName( path )
```

## Arguments
* **path** (string): The path that you want to get the file name out of.

## Return Values
* (string): The file name.

# Examples
```lua
-- Returns "level.mfk"
GetFileName("scripts\\missions\\level01\\level.mfk")
```