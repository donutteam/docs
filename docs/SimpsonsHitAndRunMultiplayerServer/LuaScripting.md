---
title: "Lua Scripting"
description: "Allows Simpsons Hit and Run Multiplayer Server mods to run Lua scripts to modify server behavior."
authors: [ 1 ]
---

The Simpsons Hit & Run Multiplayer (SHAR MP) Server has a Lua Scripting component that allows mods to modify the behavior of the server.

Mods define an entry point Lua script that is executed as soon as the mod is loaded. This script can then define functions that will be executed when certain events are fired on the server.

# Blocked Functions/Variables
For a list of all of the stock Lua functions and variables that are blocked in Simpsons Hit & Run Multiplayer Server, see [[BlockedLuaFunctionsAndVariables.md]].

# Additional Functionality

The Lua Scripting component also provides some additional functionality that mods can utilise. This functionality is provided through a set of tables that are available in the Lua environment. Each table provides functions and/or properties related to a specific area.

| Table                                 | Description                                                     |
|---------------------------------------|-----------------------------------------------------------------|
| [[LuaScripting/Cryptography.md]]      | Provides functions for performing cryptographic operations.     |
| [[LuaScripting/DateTime.md]]          | Provides functions for working with dates and times.            |
| [[LuaScripting/Directory.md]]         | Provides functions for working with directories.                |
| [[LuaScripting/Engine.md]]            | Provides functions for interacting with the game engine.        |
| [[LuaScripting/Engine.Quaternion.md]] | Provides functions for working with quaternions.                |
| [[LuaScripting/Engine.Vector3.md]]    | Provides functions for working with 3D vectors.                 |
| [[LuaScripting/Engine.VectorUtil.md]] | Provides functions for working with vectors.                    |
| [[LuaScripting/File.md]]              | Provides functions for working with the file system.            |
| [[LuaScripting/Server.md]]            | Provides functions for interacting with the multiplayer server. |
| [[LuaScripting/Server.Commands.md]]   | Provides functions for working with server commands.            |
| [[LuaScripting/Server.CurrentMod.md]] | Provides functions for working with the current mod.            |
| [[LuaScripting/Server.Players.md]]    | Provides functions for working with players on the server.      |
| [[LuaScripting/Session.md]]           | Provides functions for working with multiplayer sessions.       |
| [[LuaScripting/String.md]]            | Provides functions for working with strings.                    |
| [[LuaScripting/System.md]]            | Provides structural functions.                                  |

## Global Functions

In addition to the functions provided by the tables listed above, there are also some global functions that are available in the Lua environment. These functions are not part of any table and can be called directly.

| Function Name               | Description                                                                  |
|-----------------------------|------------------------------------------------------------------------------|
| [[LuaScripting/print_r.md]] | A function that takes a Lua object and prints it in a human-readable format. |

# Data Structures

In some cases, functions may return data structures that represent certain concepts on the server such as players and characters. These can be used to manipulate those concepts in various ways. The following data structures are currently available:

| Data Structure                        | Description                                   |
|---------------------------------------|-----------------------------------------------|
| [[DataStructures/Configuration.md]]   | Data representing the server's configuration. |
| [[DataStructures/Player.md]]          | Data representing a player on the server.     |
| [[DataStructures/PlayerCharacter.md]] | Data representing a player's character.       |