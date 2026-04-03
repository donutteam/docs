---
title: "Configuration"
description: "Provides information about the Configuration return type used in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Configuration` return type represents the server's configuration settings in Simpsons Hit & Run Multiplayer Server mods. It is returned by certain functions that retrieve configuration data from the server.

While you can modify this configuration data, most of the fields are only utilised during server startup.

## Properties
| Property Name                | Type                    | Description                                                                                                          |
|------------------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------|
| `ServerName`                 | string                  | The name of the server.                                                                                              |
| `Password`                   | string                  | The password required for clients to connect to the server. If this is an empty string, no password is required.     |
| `MaxPlayers`                 | number                  | The maximum number of players that can be connected to the server at the same time.                                  |
| `Port`                       | number                  | The port number that the server is listening on for incoming connections.                                            |
| `APIEndpoint`                | string                  | Currently unused.                                                                                                    |
| `APIKey`                     | string                  | Currently unused.                                                                                                    |
| `BroadcastServer`            | boolean                 | Whether the server is broadcast to the Donut Team server browser.                                                    |
| `AllowInGameTextChat`        | boolean                 | If true, clients are allowed to use in-game text chat. If false, in-game text chat is disabled.                      |
| `UpdateInterval`             | number                  | The interval in milliseconds at which the server updates a user.                                                     |
| `UpdateIntervalLowBandwidth` | number                  | The interval in milliseconds at which the server updates a user, if they join with the low bandwidth option enabled. |
| `EnableMods`                 | boolean                 | If true, the server's Lua environment is enabled.                                                                    |
| `ServerModificationPaths`    | HashSet                 | A set of file paths to server modifications that are loaded by the server.                                           |
| `ClientModificationPaths`    | HashSet                 | Currently unused.                                                                                                    |
| `RequiredModNames`           | HashSet                 | A set of mod names that clients are required to have in order to connect to the server.                              |
| `BannedModNames`             | HashSet                 | A set of mod names that clients are banned from having in order to connect to the server.                            |
| `RequiredModsSHA256`         | HashSet                 | Currently unused.                                                                                                    |
| `BannedModsSHA256`           | HashSet                 | Currently unused.                                                                                                    |
| `ModPermissions`             | ModPermissions          | A set of permissions that control what server-side mods are allowed to do.                                           |
| `NonSyncedGameBehaviours`    | NonSyncedGameBehaviours | A set of game behaviors that are not synchronized between clients and the server.                                    |

## ModPermissions Properties

**Added in Version 1.1.**

| Property Name  | Type    | Description                                                            |
|----------------|---------|------------------------------------------------------------------------|
| `WebRequests`  | boolean | Whether server-side mods are allowed to make HTTP requests.            |