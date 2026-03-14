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

# Notes
In the base game, Level 3 never uses the [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/fmv.md]] objective. Instead, Level 3's movie gets marked complete when you watch the Itchy & Scratchy movie after collecting all collector cards.

There is, however, nothing stopping a mod from using a [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/fmv.md]] objective in Level 3 if it wants to.