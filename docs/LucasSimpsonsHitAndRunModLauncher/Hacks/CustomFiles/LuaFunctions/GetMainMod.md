---
title: "GetMainMod"
description: "Returns the InternalName of the current main mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Returns the InternalName of the current main mod.

# Syntax
```lua
GetMainMod()
```

## Arguments
No arguments.

## Return Values
* (string | nil): The name of the current main mod or `nil` if there is no main mod enabled.

# Examples
```lua
local CurrentMainMod = GetMainMod()

if CurrentMainMod == "DonutMod3" then
    -- Donut Mod specific code.
else
    -- Whatever else you want.
end
```