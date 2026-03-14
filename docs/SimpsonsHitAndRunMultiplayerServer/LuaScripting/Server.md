---
title: "Server"
description: "Provides information about the Server table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Server` table provides information about the server and the players connected.

## Variables
| Variable Name | Type                                | Description                          |
|---------------|-------------------------------------|--------------------------------------|
| `Config`      | [[../DataStructures/Configuration.md]] | The server's configuration settings. |

## Methods
| Function Name                     | Description                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| [[Server/AddEventListener.md]]    | Registers a function to be called when a specific event occurs on the server. |
| [[Server/RemoveEventListener.md]] | Unregisters a previously registered event listener function from the server.  |
| [[Server/TriggerEvent.md]]        | Triggers a server event, calling all registered listeners for that event.     |

## Subtables
| Subtable Name            | Description                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------|
| [[Server.CurrentMod.md]] | Provides functions for managing and retrieving information about the current mod.                     |
| [[Server.Commands.md]]   | Provides functions for registering and managing server commands.                                      |
| [[Server.Players.md]]    | Provides functions for managing and retrieving information about the players connected to the server. |