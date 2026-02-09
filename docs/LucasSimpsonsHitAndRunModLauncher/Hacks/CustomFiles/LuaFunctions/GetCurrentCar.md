---
title: "GetCurrentCar"
description: "Gets what car the player is currently using."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets what mission the player is currently in.

# Syntax
```lua
GetCurrentCar()
```

## Arguments
No arguments.

## Return Values
* (string | nil): The name of the car the player is currently using or `nil` if the player does not have a car or is not in game.

# Examples
```lua
local CurrentSkin = GetCurrentSkin()
if CurrentSkin == "h_fat" then
	-- Do something if Homer is a fatass
end
```