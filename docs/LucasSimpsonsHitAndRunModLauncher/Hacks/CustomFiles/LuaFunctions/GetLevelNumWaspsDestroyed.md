---
title: "GetLevelNumWaspsDestroyed"
description: "Gets the number of wasps that the player has destroyed in the given level."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the number of wasps that the player has destroyed in the given level.

# Syntax
```lua
GetLevelNumWaspsDestroyed( level )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (integer | nil): The number of wasps the player has destroyed or `nil` if unavailable.

# Examples
```lua
local NumberOfWaspsHomerHasDestroyed = GetLEvelNumWaspsDestroyed(1)
if NumberOfWaspsHomerHasDestroyed > 15 then
	-- Do something if Homer has way too much hatred of giant alien wasps equipped with cameras
	-- ...
	-- Actually, that seems fair
end
```