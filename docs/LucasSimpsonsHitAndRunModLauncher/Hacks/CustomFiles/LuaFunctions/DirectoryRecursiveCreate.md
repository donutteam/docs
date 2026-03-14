---
title: "DirectoryRecursiveCreate"
description: "Recursively creates directories with the given path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 358 # 1.10
---

Recursively creates directories with the given path.

# Syntax
```lua
DirectoryRecursiveCreate( base_path, path )
```

## Arguments
* **base_path** (string): The path to create directories inside within the [[../VirtualFileSystem.md]].
* **path** (string): The directories to create.

## Return Values
* (boolean): Whether the directories were successfully created.

# Examples
```lua
local Created = DirectoryRecursiveCreate("/UserData/SavedGames/" .. GetModName(), "Some/Child/Directory")
```