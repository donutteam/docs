---
title: "Player:SendCreateExplosion"
description: "Provides information about the Player:SendCreateExplosion function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Creates an explosion at the specified location with the given parameters and sends it to the player.

# Syntax
```lua
Player:SendCreateExplosion( position )
```

## Arguments
* **position** ([[../../LuaScripting/Engine.Vector3.md|Vector3]]): The position where the explosion will be created.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
local position = Engine.Vector3(1, 2, 3)
player:SendCreateExplosion(position)
```