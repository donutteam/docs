---
title: "GetModPath"
description: "Returns the path to a mod within the Virtual File System."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Returns the path to a mod within the [[../VirtualFileSystem.md]].

# Syntax
```lua
GetModPath( [mod_name] )
```

## Arguments
* **mod_name** (string): Specify the InternalName of a mod whose path you want to get.
    * Optional, defaults to the mod that called the function.
    * This function always returns a path regardless of whether or not the specified mod name is valid or enabled.

## Return Values
* (string): The path to the mod.

# Examples
```lua
-- Get the current mod's path.
-- Returns "/Mods/CurrentMod"
local Path = GetModPath()

-- Get Donut Mod's path
local Path = GetModPath("DonutMod3")
```