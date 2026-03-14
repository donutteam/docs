---
title: "Server.Players"
description: "Provides information about the Server.Players table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Server.Players` table provides functionality for managing and retrieving information about the players connected to the server.

## Variables
This table does not have any variables.

## Methods
| Function Name                         | Description                                                      |
|---------------------------------------|------------------------------------------------------------------|
| [[Server.Players/GetPlayers.md]]      | Returns a list of all players currently connected to the server. |
| [[Server.Players/GetPlayersWhere.md]] | Returns a list of players that match the specified criteria.     |
| [[Server.Players/GetPlayer.md]]       | Returns a player object for the player with the specified ID.    |