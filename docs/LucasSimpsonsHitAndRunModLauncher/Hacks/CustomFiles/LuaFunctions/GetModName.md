---
title: "GetModName"
description: "Returns the InternalName of the current mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Returns the `InternalName` of the current mod.

# Syntax
```lua
GetModName()
```

## Arguments
No arguments.

## Return Values
* (string): The `InternalName` of the current mod.

# Examples
```lua
-- Prints the InternalName of the mod that called it.
print(GetModName())
```