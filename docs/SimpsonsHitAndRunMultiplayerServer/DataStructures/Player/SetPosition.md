---
title: "Player:SetPosition"
description: "Provides information about the Player:SetPosition function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Sets the player's current position. Their dynaload data will be updated to reflect their new position.

# Syntax
```lua
Player:SetPosition( position )
```

## Arguments
* **position** ([[../../LuaScripting/Engine.Vector3.md|Vector3]]): The new position to set for the player.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
local newPosition = Engine.Vector3(1, 2, 3)
player:SetPosition(newPosition)
```