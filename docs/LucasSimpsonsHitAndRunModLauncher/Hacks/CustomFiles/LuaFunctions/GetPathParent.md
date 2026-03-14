---
title: "GetPathParent"
description: "Returns the parent path of the specified file path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 355 # 1.8
---

Returns the parent path of the specified file path.

This will return the file name if it is only given a file name.

# Syntax
```lua
GetPathParent( path, [windows] )
```

## Arguments
* **path** (string): The file path that you want to get the parent path out of.
* **windows** (boolean): Whether to parse the path using backslashes.
    * Optional, defaults to true.

## Return Values
* (string): The parent path.

# Examples
```lua
-- Returns "scripts\missions\level01"
GetPathParent("scripts\\missions\\level01\\level.mfk")

-- Returns "level.mfk"
GetPathParent("level.mfk")
```