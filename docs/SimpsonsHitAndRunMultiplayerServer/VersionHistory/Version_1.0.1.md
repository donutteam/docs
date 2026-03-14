---
title: "Version 1.0.1"
description: "Changelog for Version 1.0.1 of the Simpsons Hit & Run Multiplayer Server."
authors: [ 1 ]
---

**This version was released on March 14th, 2026.**

# Server Software

## General
- Added messaging for when a player is in the process of joining. This message will show up for all players who match the joining player's main mod.
- Fixed an issue where the server would not properly indicate a player has left until after a timeout period, which could lead to confusion when players were disconnected.
- Fixed an issue where when you joined the server, a blip would be placed on your radar at the center of the world.
- Fixed an issue where when you spawned a radar icon, it would not be sent to other players.

## Configuration
- Added the `useChatFilter` configuration option, which allows server owners to enable or disable the built-in chat filter. Defaults to `true`.

## Lua Scripting
- Added the `PlayerCheated` event, which is triggered when a player is detected cheating.
- Fixed an issue that prevented mods from looking up players.

## Known Issues

- There is a random crash that can occur during normal gameplay. The cause of this crash is currently unknown, but it is being investigated.

# SHAR MP Companion Mod

- Fixed an issue that allowed the `tp` command to try teleporting to a player that is not part of your session. 