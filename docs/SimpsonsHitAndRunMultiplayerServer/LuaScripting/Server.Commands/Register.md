---
title: "Server.Commands.Register"
description: "Provides information about the Server.Commands.Register function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Adds a new chat command that players can use in the game chat. When a player types the command in chat, the provided callback function will be called with the player who sent the command and any arguments they provided.

# Syntax
```lua
Server.Commands.Register( name, minimumArgs, maximumArgs, usage, callback )
```
## Arguments
* **name** (string): The name of the command. This is the word that players will type in chat to use the command, without the leading slash.
* **minimumArgs** (number): The minimum number of arguments required for the command. If a player tries to use the command with fewer arguments than this, they will receive an error message.
* **maximumArgs** (number): The maximum number of arguments allowed for the command. If a player tries to use the command with more arguments than this, they will receive an error message.
* **usage** (string): A string describing how to use the command. This will be shown to players if they use the command incorrectly (e.g. with the wrong number of arguments).
* **callback** (function): The function to call when the command is used. This function will be passed the following arguments:
  * **player** (Player): The player who sent the command.
  * **args** (table): A table of the arguments provided by the player, where `args[1]` is the first argument, `args[2]` is the second argument, and so on.
  * **argsN** (number): The total number of arguments provided by the player.

## Return Values
No return values.

# Examples
```lua
Server.Commands.Register("hide", 0, 0, "/hide",
function (player, args, argsN)
    player.Character.HasRadarIcon = not player.Character.HasRadarIcon
    player.Character.HasNameTag = not player.Character.HasNameTag
    player.Character.HasFullScreenMapIcon = not player.Character.HasFullScreenMapIcon
    player:SendGameChatMessage("Your radar icon and name tag are now " .. (player.Character.HasRadarIcon and "visible" or "hidden"))
end)
```
