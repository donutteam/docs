---
title: "IsLevelStreetRaceCompleted"
description: "Checks if the given street race is completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given street race is completed.

# Syntax
```lua
IsLevelStreetRaceCompleted( level, mission )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
* **mission** (integer): The street race to check.
	* Between 1 and 3 *or* the max `StreetRaces` set for the level by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (boolean | nil): If the player has completed the street race or `nil` if unavailable.

# Examples
```lua
local MilhouseRaceCompleted = IsLevelStreetRaceCompleted(1, 1)
if MilhouseRaceCompleted then
	-- Do something if Homer has completed Milhouse's race
end
```