---
title: "Player:SendCreateMissionRadarIcon"
description: "Provides information about the Player:SendCreateMissionRadarIcon function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Sets the current mission radar icon position for the player.

# Syntax
```lua
Player:SendCreateMissionRadarIcon( position )
```

## Arguments
* **position** (Vector3): The new position to set for the player's mission radar icon.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
local newPosition = Engine.Vector3(1, 2, 3)
player:SendCreateMissionRadarIcon(newPosition)
```