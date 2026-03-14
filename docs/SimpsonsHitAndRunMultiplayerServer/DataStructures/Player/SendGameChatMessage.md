---
title: "Player:SendGameChatMessage"
description: "Provides information about the Player:SendGameChatMessage function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Sends a chat message to the player.

# Syntax
```lua
Player:SendGameChatMessage( playerCharacter, message )
Player:SendGameChatMessage( message )
```

## Arguments
* **playerCharacter** (PlayerCharacter): The player character that has sent the message.
* **message** (string): The chat message sent by the player.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
local playerCharacter = --[[ get player character reference ]]
local message = "Hello, world!"
player:SendGameChatMessage(playerCharacter, message)
player:SendGameChatMessage(message)
```