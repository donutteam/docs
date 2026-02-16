---
title: "IsLevelWagerRaceCompleted"
description: "Checks if the given wager race is completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given wager race is completed.

# Syntax
```lua
IsLevelGambleRaceCompleted( level )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (boolean | nil): If the player has completed the level's wager race or `nil` if unavailable.

# Examples
```lua
local GambleRaceCompleted = IsLevelGambleRaceCompleted(1)
if GambleRaceCompleted then
	-- Do something if Homer has completed a wager with the mob
end
```