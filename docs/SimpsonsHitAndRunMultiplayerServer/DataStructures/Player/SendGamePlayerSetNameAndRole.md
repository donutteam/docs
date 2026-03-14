---
title: "Player:SendGamePlayerSetNameAndRole"
description: "Provides information about the Player:SendGamePlayerSetNameAndRole function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

An internal method used by the server to update the player's name and role. This is not intended for use in mods.

# Syntax
```lua
Player:SendGamePlayerSetNameAndRole()
```

## Arguments
No arguments.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
player:SendGamePlayerSetNameAndRole()
```