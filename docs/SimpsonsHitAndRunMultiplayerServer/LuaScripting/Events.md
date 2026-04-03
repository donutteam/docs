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

| Value Name | Type                            | Description                        |
|------------|---------------------------------|------------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that joined the server. |

## `PlayerKicked`
Triggered when a player is kicked from the server.

| Value Name | Type                            | Description                                 |
|------------|---------------------------------|---------------------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that was kicked from the server. |
| Message    | string                          | The reason for the kick.                    |

## `PlayerChangedSession`
Triggered when a player changes their session

| Value Name | Type                            | Description                            |
|------------|---------------------------------|----------------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that changed their session. |
| Session    | [[Session.md]]                  | The new session the player has joined. |

## `PlayerGameStarted`
Triggered when a player starts a game.

| Value Name | Type                                     | Description                             |
|------------|------------------------------------------|-----------------------------------------|
| Client     | [[../DataStructures/Player.md]]          | The player that started a game.         |
| Character  | [[../DataStructures/PlayerCharacter.md]] | The character the player is playing as. |
| Level      | Level                                    | The level the player is playing in.     |
| Session    | [[Session.md]]                           | The session the player is playing in.   |

## `PlayerGameEnded`
Triggered when a player ends a game.

| Value Name | Type                            | Description                   |
|------------|---------------------------------|-------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that ended a game. |

## `GameTick`
Triggered on every game tick (approximately every 50ms).

| Value Name | Type   | Description                                                           |
|------------|--------|-----------------------------------------------------------------------|
| count      | number | The number of game ticks that have occurred since the server started. |
| time       | number | The total time in seconds that has elapsed since the server started.  |

## `PlayerAssaulted`
Triggered when a player is assaulted by another player (kicked)

| Value Name | Type                            | Description                                   |
|------------|---------------------------------|-----------------------------------------------|
| Assailer   | [[../DataStructures/Player.md]] | The player that initiated the assault.        |
| Victim     | [[../DataStructures/Player.md]] | The player that was assaulted.                |
| Distance   | number                          | The distance between the assailer and victim. |

## `PlayerJumped`
Triggered when a player jumps in-game.

| Value Name | Type                            | Description             |
|------------|---------------------------------|-------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that jumped. |

## `PlayerCheated`
**Added in 1.0.1**

Triggered when a player is detected cheating.

| Value Name | Type                            | Description                            |
|------------|---------------------------------|----------------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that was detected cheating. |

## `MessageReceived`
**Added in 1.1**

Triggered when a player sends a chat message.

The `Message` field can be modified to change the content of the message before it is sent to other players. Setting `Censor` to `false` will prevent the message from being passed through the built-in chat filter.

| Value Name | Type                            | Description                                                          |
|------------|---------------------------------|----------------------------------------------------------------------|
| Client     | [[../DataStructures/Player.md]] | The player that sent the message.                                    |
| Message    | string                          | The message that was sent. Can be modified to change the content.    |
| Censor     | boolean                         | Whether to apply the chat filter to the message. Defaults to `true`. |
