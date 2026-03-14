---
title: "IsLevelMissionCompleted"
description: "Checks if the given story mission is completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given story mission is completed.

# Syntax
```lua
IsLevelMissionCompleted( level, mission )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
* **mission** (integer): The mission to check.
	* For Level 1, between 0 and 7 *or* the max `StoryMissions` set for the level by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
	* For Levels 2-7, between 1 and 8 *or* the max `StoryMissions` set for the level by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (boolean | nil): If the player has completed the mission or `nil` if unavailable.

# Examples
```lua
local FatAndFuriousCompleted = IsLevelMissionCompleted(1, 7)
if FatAndFuriousCompleted then
	-- Do something if Homer has thwarted Burns' plans
end
```