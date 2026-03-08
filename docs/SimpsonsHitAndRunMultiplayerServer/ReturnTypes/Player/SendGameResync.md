---
title: "Player:SendGameResync"
description: "Provides information about the Player:SendGameResync function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Resynchronizes the game state for the player.

# Syntax
```lua
Player:SendGameResync()
```

## Arguments
No arguments.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
player:SendGameResync()
```