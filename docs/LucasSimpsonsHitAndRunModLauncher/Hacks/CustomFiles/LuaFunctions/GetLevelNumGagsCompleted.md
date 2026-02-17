---
title: "GetLevelNumGagsCompleted"
description: "Gets the number of gags that the player has completed in the given level."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the number of gags that the player has completed in the given level.

# Syntax
```lua
GetLevelNumGagsCompleted( level )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (integer | nil): The number of gags the player has completed or `nil` if unavailable.

# Examples
```lua
local NumberOfGagsHomerHasCompleted = GetLevelNumGagsCompleted(1)
if NumberOfGagsHomerHasCompleted > 15 then
	-- Do something if Homer has enjoyed 15 or more funny Simpsons moments
end
```