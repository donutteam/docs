---
title: "GetLevelCount"
description: "Gets how many levels the game has."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets how many levels the game has.

# Syntax
```lua
GetLevelCount()
```

## Arguments
No arguments.

## Return Values
* (integer): How many levels the game has.
	* This is affected by the `Levels` set by the [[../../CustomStatsTotals.md]] hack, if it is loaded.
	* Otherwise, it will return 7.

# Examples
```lua
local LevelCount = GetLevelCount()
if LevelCount >= 3 then
	-- Definitely safe to use other CF functions for Level 3+ here
end
```