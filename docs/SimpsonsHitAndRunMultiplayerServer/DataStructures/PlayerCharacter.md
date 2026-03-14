---
title: "PlayerCharacter"
description: "Provides information about the PlayerCharacter return type used in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `PlayerCharacter` return type represents a player's character in Simpsons Hit & Run Multiplayer Server mods. It is returned by certain functions that retrieve player character data from the server.

## Variables
| Variable Name          | Type    | Description                                                      |
|------------------------|---------|------------------------------------------------------------------|
| `HasRadarIcon`         | boolean | If true, the player is visible on the radar.                     |
| `HasFullScreenMapIcon` | boolean | If true, the player is visible on the full screen map.           |
| `HasNameTag`           | boolean | If true, the player's name tag is visible above their character. |

## Methods
| Function Name                      | Description                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[PlayerCharacter/GetPosition.md]] | Gets the player's character's current position in the level. This is null if the player is not currently in a level. |