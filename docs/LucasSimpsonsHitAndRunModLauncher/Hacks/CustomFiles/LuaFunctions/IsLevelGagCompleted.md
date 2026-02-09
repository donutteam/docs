---
title: "IsLevelGagCompleted"
description: "Checks if the given gag in a level has been completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given gag in a level has been completed.

# Syntax
```lua
IsLevelGagCompleted( level, gag )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
* **gag** (integer): The gag to check.
	* Between 1 and 32 (the max amount of gags in a level).

## Return Values
* (boolean | nil): If the player has completed the gag or `nil` if unavailable.

# Examples
```lua
-- This is the 3rd persistent gag added to Level 1 in the base game
local FlandersBombShelterCompleted = IsLevelGagCompleted(1, 3)
if FlandersBombShelterCompleted then
	-- Do something if Homer has compromised the integrity of Flanders' bomb shelter
end
```

# Notes
Gag indices correspond to the order persistent gags (those that call [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/GagSetPersist.md]] to count towards the gag total) are added in the level's load script.