---
title: "Events"
description: "Provides information about the events available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

This page lists all the events that can be listened for in Simpsons Hit & Run Multiplayer Server mods using the [[Server/AddEventListener.md]] function.

## `PlayerJoined`
Triggered when a player joins the server.

| Value Name | Type   | Description                        |
|------------|--------|------------------------------------|
| Client     | Player | The player that joined the server. |

## `PlayerKicked`
Triggered when a player is kicked from the server.

| Value Name | Type   | Description                                 |
|------------|--------|---------------------------------------------|
| Client     | Player | The player that was kicked from the server. |
| Message    | string | The reason for the kick.                    |

## `PlayerChangedSession`
Triggered when a player changes their session

| Value Name | Type    | Description                            |
|------------|---------|----------------------------------------|
| Client     | Player  | The player that changed their session. |
| Session    | Session | The new session the player has joined. |

## `PlayerGameStarted`
Triggered when a player starts a game.

| Value Name | Type            | Description                             |
|------------|-----------------|-----------------------------------------|
| Client     | Player          | The player that started a game.         |
| Character  | PlayerCharacter | The character the player is playing as. |
| Level      | Level           | The level the player is playing in.     |
| Session    | Session         | The session the player is playing in.   |

## `PlayerGameEnded`
Triggered when a player ends a game.

| Value Name | Type   | Description                   |
|------------|--------|-------------------------------|
| Client     | Player | The player that ended a game. |

## `GameTick`
Triggered on every game tick (approximately every 50ms).

| Value Name | Type   | Description                                                           |
|------------|--------|-----------------------------------------------------------------------|
| count      | number | The number of game ticks that have occurred since the server started. |
| time       | number | The total time in seconds that has elapsed since the server started.  |

## `PlayerAssaulted`
Triggered when a player is assaulted by another player (kicked)

| Value Name | Type   | Description                                   |
|------------|--------|-----------------------------------------------|
| Assailer   | Player | The player that initiated the assault.        |
| Victim     | Player | The player that was assaulted.                |
| Distance   | number | The distance between the assailer and victim. |

## `PlayerJumped`
Triggered when a player jumps in-game.

| Value Name | Type   | Description             |
|------------|--------|-------------------------|
| Client     | Player | The player that jumped. |

## `PlayerCheated`
**Added in 1.0.1**

Triggered when a player is detected cheating.

| Value Name | Type   | Description                            |
|------------|--------|----------------------------------------|
| Client     | Player | The player that was detected cheating. |
