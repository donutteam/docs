---
title: "GetCurrentLevel"
description: "Gets what level of the game the player is currently in."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets what level of the game the player is currently in.

# Syntax
```lua
GetCurrentLevel()
```

## Arguments
No arguments.

## Return Values
* (integer | nil): The current level or `nil` if the player is not in game.

# Examples
```lua
local CurrentLevel = GetCurrentLevel()
if CurrentLevel == 7 then
	-- Do Spooky Scary Stuff Here
end
```