---
title: "GetActiveLevelMission"
description: "Gets the player's active level and story mission."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the player's active level and story mission.

# Syntax
```lua
GetActiveLevelMission()
```

## Arguments
No arguments.

## Return Values
* (integer | nil): The player's active level or `nil` if unavailable.
* (integer | nil): The player's active story mission or `nil` if unavailable.

# Examples
```lua
local ActiveLevel, ActiveStoryMission = GetActiveLevelMission()
if ActiveLevel == 3 and ActiveStoryMission == 3 then
	-- Do something different if the player is on Level 3 Mission 3 in some manner
end
```

# Notes
When in a bonus mission or street race, this will return the same story mission the player would return to upon cancelling or completing the bonus mission or street race.