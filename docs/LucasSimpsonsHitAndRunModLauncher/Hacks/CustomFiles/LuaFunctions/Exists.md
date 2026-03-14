---
title: "Exists"
description: "Returns whether or not the specified path exists."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Returns whether or not the specified path exists.

# Syntax
```lua
Exists ( path, is_file, is_directory )
```

## Arguments
* **path** (string): The path to check.
* **is_file** (boolean): Return true if the path is a file. 
* **is_directory** (boolean): Return true if the path is a directory.

## Return Values
* (boolean): Whether the file exists.

# Examples
```lua
if Exists(GetModPath() .. "/Resources/test.lua", true, false) then
    -- do stuff if that file exists
end
```