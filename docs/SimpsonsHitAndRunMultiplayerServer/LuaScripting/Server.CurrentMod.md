---
title: "Server.CurrentMod"
description: "Provides information about the Server.CurrentMod table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Server.CurrentMod` table provides variables for managing and retrieving information about the current mod on the server.

## Variables
| Variable Name  | Type    | Description                                |
|----------------|---------|--------------------------------------------|
| `internalName` | string  | The internal name of the current mod.      |
| `title`        | string  | The display title of the current mod.      |
| `description`  | string  | A description of the current mod.          |
| `version`      | string  | The version of the current mod.            |
| `entryPoint`   | string  | The entry point script of the current mod. |
| `debug`        | boolean | Whether the current mod is in debug mode.  |

## Methods
This table does not have any methods.