---
title: "Version 1.1"
description: "Changelog for Version 1.1 of the Simpsons Hit & Run Multiplayer Server."
authors: [ 1 ]
---

**This version was released on April 3rd, 2026.**

# Server Software

## Important Note
- To prevent complications with the Mod Launcher, we've opted to rename the Mods path from `Mods` to `ServerMods`. This change will require all server owners to move their mods from the old `Mods` folder to the new `ServerMods` folder. We apologize for any inconvenience this may cause, but we believe this change will lead to less issues in the long run.

## New Features
- Added the ability to broadcast your server to a Donut Team server browser.
    - The first iteration of the server browser will only be available in from launcher.donutteam.com. We will be adding it directly into the Mod Launcher in a future update.
    - In order for your server to be listed on the server browser, it will need to be able to communicate with launcher.donutteam.com and will also need to be able to listen for incoming TCP connections on the same port that your game server is running on. If your server is behind a NAT, you will likely need to set up port forwarding in order for it to be listed on the server browser.
- Added the `/broadcast-server <true|false>` command, which allows server operators to enable or disable broadcasting their server to the Donut Team server browser.    
- Added the `HTTP` Lua module, allowing scripts to make HTTP requests from the server. Servers must enable the `WebRequests` permission in their Server.yaml file in order for HTTP requests to be allowed.
- Added the `String.ToJSON` Lua function, which allows scripts to convert a Lua table to a JSON string.
- Added the `MessageReceived` event to the server Lua API, which allows scripts to handle incoming chat messages from players.

## Bug Fixes
- Fixed configuration not saving after loading, meaning new keys added to the configuration (by the server) would not persist after a server restart
- Fixed an issue where kick messages were not correctly telling the player that they had been kicked.
- Fixed single quotes in command input parsing
- Fixed an issue where `Server.Players.GetPlayersWhere` was not handling keywords in a case-insensitive manner.
- Instead of censoring inappropriate names, the server will now reject players attempting to join with a name that contains inappropriate content.

# SHAR MP Companion Mod
- Added a migration to add a username and discriminator field to the banned users table.
- Added the `/unban` command, which allows server operators to unban a previously banned user by specifying their username and discriminator.
- Added the `/countdown` command, which allows players to set a countdown timer that will be visible to all players in your session. This can be useful for coordinating the start of a race.
- Fixed an issue where the `/ban` command required quotes for the reason parameter, so that banning a user with a reason containing spaces would fail unless the reason was wrapped in quotes.
- Fixed an issue where the `/kick` command required quotes for the reason parameter, so that kicking a user with a reason containing spaces would fail unless the reason was wrapped in quotes.