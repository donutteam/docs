---
title: "Player:SetDynaloadData"
description: "Provides information about the Player:SetDynaloadData function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Sets the player's current dynaload data. This is used to control which parts of the level are loaded for the player.

# Syntax
```lua
Player:SetDynaloadData( dynaloadData )
```

## Arguments
* **dynaloadData** (string): The new dynaload data to set for the player.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
player:SetDynaloadData("l1z3.p3d;l1r2.p3d;l1r3.p3d;")
```