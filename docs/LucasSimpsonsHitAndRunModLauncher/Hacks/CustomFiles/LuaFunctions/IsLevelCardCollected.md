---
title: "IsLevelCardCollected"
description: "Checks if the given card has been collected in a level."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given card has been collected in a level.

# Syntax
```lua
IsLevelCardCollected( level, card )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
* **card** (integer): The card to check.
	* Between 1 and 7 *or* the max `CollectorCards` set for the level by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (boolean | nil): If the player has collected the card or `nil` if unavailable.

# Examples
```lua
local FootballCardCollected = IsLevelCardCollected(1, 1)
if FootballCardCollected then
	-- Do something if Homer has collected the football card
end
```