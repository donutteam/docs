---
title: "GetModVersion"
description: "Returns the version of the specified mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

Returns the version of the specified mod.

# Syntax
```lua
GetModVersion( [mod_name] )
```

## Arguments
* **mod_name** (string): The name of the mod whose version you'd like to get.
    * Optional, defaults to the mod that called the function.

## Return Values
* (string | nil): The version of the mod or `nil` if it does not have a version or is not loaded.

# Examples
```lua
local CurrentModVersion = GetModVersion()

print("Version " .. CurrentModVersion .. " loaded!")
```