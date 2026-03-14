---
title: "GetCurrentMission"
description: "Gets what mission the player is currently in."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets what mission the player is currently in.

# Syntax
```lua
GetCurrentMission()
```

## Arguments
No arguments.

## Return Values
* (string | nil): The internal name of the mission the player is currently in or `nil` if the player is not in game.
* (integer | nil): The index of the mission the player is currently in or `nil` if the player is not in game.

# Examples
```lua
local CurrentMissionName, CurrentMissionIndex = GetCurrentMission()
if CurrentMissionName == "m1sd" then
	-- Do something here if this path handler is executed during the first mission's sunday drive
elseif CurrentMissionName == "m1" then
	-- Do something else if it is executed during the actual mission
end
```