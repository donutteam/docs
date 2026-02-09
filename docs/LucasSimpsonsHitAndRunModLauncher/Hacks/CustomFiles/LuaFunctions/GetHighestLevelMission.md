---
title: "GetHighestLevelMission"
description: "Gets the highest level and story mission the player has reached."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the highest level and story mission the player has reached.

# Syntax
```lua
GetHighestLevelMission()
```

## Arguments
No arguments.

## Return Values
* (integer | nil): The highest level the player has reached or `nil` if unavailable.
* (integer | nil): The highest story mission the player has reached or `nil` if unavailable.

# Examples
```lua
local HighestLevel, HighestStoryMission = GetActiveLevelMission()
if HighestLevel == 3 and HighestStoryMission == 3 then
	-- Do something different if the player has reached at least Level 3 Mission 3
end
```