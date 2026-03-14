---
title: "GetModTitle"
description: "Returns the title of the specified mod or the current mod if none is specified."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

Returns the title of the specified mod or the current mod if none is specified.

# Syntax
```lua
GetModTitle( [mod_name] )
```

## Arguments
* **mod_name** (string): The name of the mod whose title you'd like to get.
    * Optional, defaults to the mod that called the function.

## Return Values
* (string | nil): The title of the mod or `nil` if it is not loaded.

# Examples
```lua
local CurrentModTitle = GetModTitle()

print(CurrentModTitle .. " loaded!")
```