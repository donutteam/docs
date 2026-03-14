---
title: "IsHackLoaded"
description: "Checks whether a hack is loaded."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 370 # 1.15.2
---

Checks whether a hack is loaded.

# Syntax
```lua
IsHackLoaded( hack_name )
```

## Arguments
* **hack_name** (string): The `InternalName` of the hack.

## Return Values
* (boolean): Whether the hack is loaded.

# Examples
```lua
-- Will always return true because Hack Support is always enabled
print(IsHackLoaded("HackSupport"))

-- Check if CustomShopSupport is loaded
print(IsHackLoaded("CustomShopSupport"))

-- Mod Hacks can be checked with this or IsModEnabled
print(IsHackLoaded("DebugText"))
```