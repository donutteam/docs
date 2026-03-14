---
title: "Player:SendGamePlayerCharacterJump"
description: "Provides information about the Player:SendGamePlayerCharacterJump function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Tells the player that another player's character has jumped. This is used internally by the server and is not intended for use in mods.

# Syntax
```lua
Player:SendGamePlayerCharacterJump( playerCharacter )
```

## Arguments
* **playerCharacter** (PlayerCharacter): The player character that has jumped.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
local playerCharacter = --[[ get player character reference ]]
player:SendGamePlayerCharacterJump(playerCharacter)
```