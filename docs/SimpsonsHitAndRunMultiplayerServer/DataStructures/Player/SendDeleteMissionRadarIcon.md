---
title: "Player:SendDeleteMissionRadarIcon"
description: "Provides information about the Player:SendDeleteMissionRadarIcon function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Removes the current mission radar icon for the player.

# Syntax
```lua
Player:SendDeleteMissionRadarIcon()
```
 
## Arguments
No arguments.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
player:SendDeleteMissionRadarIcon()
```