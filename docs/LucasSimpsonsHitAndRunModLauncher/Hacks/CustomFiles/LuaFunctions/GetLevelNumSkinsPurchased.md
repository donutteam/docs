---
title: "GetLevelNumSkinsPurchased"
description: "Gets the number of skins that the player has purchased in the given level."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the number of for skins that the player has purchased in the given level.

# Syntax
```lua
GetLevelNumSkinsPurchased( level )
```

## Arguments
* **level** (integer): The level to check.
	* Between 1 and 7 *or* the max `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.

## Return Values
* (integer | nil): The number of skins the player has purchased or `nil` if unavailable.

# Examples
```lua
local NumberOfSkinsHomerHasBought = GetLevelNumSkinsPurchased(1)
if NumberOfSkinsHomerHasBought ~= nil and NumberOfSkinsHomerHasBought > 2 then
	-- Do something now that Homer has way too many clothes for one man
end
```