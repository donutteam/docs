---
title: "Player"
description: "Provides information about the Player return type used in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Player` return type represents a player that is currently connected to the server in Simpsons Hit & Run Multiplayer Server mods. It is returned by certain functions that retrieve player data from the server.

## Variables
| Variable Name              | Type                                           | Description                                                                                          |
|----------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------------|
| `ServerGuid`               | string                                         | The server GUID of the player.                                                                       |
| `IsCLI`                    | boolean                                        | Whether the player is a CLI player.                                                                  |
| `IsOP`                     | boolean                                        | Whether the player is an operator.                                                                   |
| `Mutators`                 | List                                           | A list of the mutators that the player has enabled.                                                  |
| `IPAddress`                | string                                         | The IP address of the player.                                                                        |
| `Name`                     | string                                         | The name of the player, including the discriminator.                                                 |
| `NameWithoutDiscriminator` | string                                         | The name of the player without the discriminator.                                                    |
| `Discriminator`            | string                                         | The discriminator of the player.                                                                     |
| `Colour`                   | number                                         | The colour of the player, represented as a hexadecimal RGB value.                                    |
| `SelectedMainMod`          | MainMod                                        | The main mod that the player has selected.                                                           |
| `Level`                    | Level                                          | The level that the player is currently in.                                                           |
| `Session`                  | [[../LuaScripting/Session.md]]                 | The session that the player is currently in.                                                         |
| `Mods`                     | List                                           | A list of the mods that the player has.                                                              |
| `Character`                | [[PlayerCharacter.md]]                         | Details about the player's character.                                                                |
| `LowBandwidth`             | boolean                                        | Whether the player has joined with the low bandwidth option enabled.                                 |
| `Data`                     | Dictionary                                     | A dictionary that can be used to store custom data for the player.                                   |
| `Ping`                     | number                                         | The player's current ping to the server, in milliseconds.                                            |
| `ExplosionMutator`         | boolean                                        | Whether the player has the explosion mutator enabled.                                                |
| `HitAndRunMutator`         | boolean                                        | Whether the player has the Hit & Run mutator enabled.                                                |
| `AllowCheaterTags`         | boolean                                        | Whether the player allows cheater tags to be shown on their name.                                    |
| `Position`                 | [[../LuaScripting/Engine.Vector3.md]] or `nil` | The player's current position in the level. This is `nil` if the player is not currently in a level. |

## Methods

| Function Name                              | Description                                                                                                               |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [[Player/SetPosition.md]]                  | Sets the player's position in the level.                                                                                  |
| [[Player/SetDynaloadData.md]]              | Sets the player's dynaload data. Dynaload data is used to determine which objects are loaded for the player in the level. |
| [[Player/SendCreateMissionRadarIcon.md]]   | Sends a command to the client to create a mission radar icon at the specified position.                                   |
| [[Player/SendDeleteMissionRadarIcon.md]]   | Sends a command to the client to delete the player's mission radar icon.                                                  |
| [[Player/Kick.md]]                         | Kicks the player from the server with an optional kick message.                                                           |
| [[Player/ChangeSession.md]]                | Moves the player to a different session.                                                                                  |
| [[Player/SendGamePlayerSetNameAndRole.md]] | Sends a command to the client to update the player's name and role in the game.                                           |
| [[Player/SendGameResync.md]]               | Sends a command to the client to resync the player's game state.                                                          |
| [[Player/SendGamePlayerCharacterJump.md]]  | Sends a command to other clients to make the player's character perform a jump action.                                    |
| [[Player/SendGamePlayerCharacterKick.md]]  | Sends a command to other clients to make the player's character perform a kick action with the specified kick force.      |
| [[Player/SendCreateExplosion.md]]          | Sends a command to other clients to create an explosion at the specified position.                                        |
| [[Player/SendGameChatMessage.md]]          | Sends a chat message to the client, either as a message from a player's character or as a server message.                 |