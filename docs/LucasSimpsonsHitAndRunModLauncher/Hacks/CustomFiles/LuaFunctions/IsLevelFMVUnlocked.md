---
title: "IsLevelFMVUnlocked"
description: "Checks if the FMV for the given level has been unlocked."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the FMV for the given level has been unlocked.

# Syntax
```lua
IsLevelFMVUnlocked( level )
```

## Arguments
* **level** (integer): The level to check.

## Return Values
* (boolean | nil): Whether the given level's FMV has been unlocked or `nil` if unavailable.

# Examples
```lua
local HasBeenSexyWhileParanoid = IsLevelFMVUnlocked(1)
if HasBeenSexyWhileParanoid then
	-- Do something now that Homer has been sexy while paranoid
end
```