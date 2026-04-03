---
title: "Configuration"
description: "This page documents the configuration file for the Simpsons Hit & Run Multiplayer Server."
authors: [ 2, 1 ]
---

This page documents the configuration file for the Simpsons Hit & Run Multiplayer Server.

You can either manually create a `Server.yaml` file or the server will generate one on first launch.

You can also pass in a custom path to a configuration file using the `--config` [[CommandLineArguments.md|command line argument]].

# Options
## serverName
**Added in Version 1.0.**

The name of the server.

**Type**: `string`

**Default**: `My SHAR MP "Server"`

## password
**Added in Version 1.0.**

The password to the server. Use a blank string to have no password.

**Type**: `string`

**Default**: `''`

## port
**Added in Version 1.0.**

The port the server will bind to.

**Type**: `integer`

**Default**: `7777`

## maxPlayers
**Added in Version 1.0.**

The maximum amount of connected players.

**Type**: `integer`

**Default**: `32`

## masterServer
**Added in Version 1.1.**

The URL of the master server that the Simpsons Hit & Run Multiplayer Server will communicate with in order to register itself and be discoverable in the server browser.

**Type**: `string`

**Default**: `'https://launcher.donutteam.com'`

## masterServerAuthorisation
**Added in Version 1.1.**

The authorisation token that the Simpsons Hit & Run Multiplayer Server will use when communicating with the master server in order to register itself and be discoverable in the server browser.

You can get your authorisation token from the Token section of your account authentication page: https://donutteam.com/settings/authentication

**Type**: `string`

**Default**: `''`

## broadcastServer
**Added in Version 1.0.**

Sets whether the server is broadcast to the Donut Team server browser, making it publicly listed and discoverable.

In order for the server to be listed, it must be able to communicate with `launcher.donutteam.com` and listen for incoming TCP connections on the same port as the game server. If the server is behind a NAT, port forwarding will likely be required. You are also required to have a valid masterServerAuthorisation value configured in order for the server to be listed.

**Type**: `boolean`

**Default**: `False`

## allowInGameTextChat
**Added in Version 1.0.**

Set whether to allow players to chat ingame.

When disabled, players will not be able to send chat messages, however commands are still allowed.

**Type**: `boolean`

**Default**: `True`

## useChatFilter
**Added in Version 1.0.1.**

Set whether to use the built-in chat filter.

When disabled, players will be able to send messages containing any content, including potentially offensive language. Enabling this option will attempt to filter out inappropriate language from chat messages.

**Type**: `boolean`

**Default**: `True`

## updateInterval
**Added in Version 1.0.**

Sets how often the server sends packets to clients, in milliseconds.

**Type**: `integer`

**Default**: `60`

## updateIntervalLowBandwidth
**Added in Version 1.0.**

Sets how often the server sends packets to clients with the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/Multiplayer.md]] hack's **Server > Low Bandwidth** setting enabled.

**Type**: `integer`

**Default**: `400`

## enableMods
**Added in Version 1.0.**

Sets if server-side mods are enabled.

**Type**: `boolean`

**Default**: `True`

## serverModificationPaths
**Added in Version 1.0.**

A list of additional paths to load server-side mods from.

**Type**: `string[]`

**Default**: `[]`

## clientModificationPaths
**Added in Version 1.0.**

Unused. Reserved for future use.

**Type**: `string[]`

**Default**: `[]`

## requiredModNames
**Added in Version 1.0.**

A list of required mod `InternalName`s that clients must have enabled in order to connect.

Leaving this empty means no mods are specifically required.

**Type**: `string[]`

**Default**: `[]`

## bannedModNames
**Added in Version 1.0.**

A list of disallowed mod `InternalName`s that will prevent clients from connecting if they are enabled.

**Type**: `string[]`

**Default**: `[]`

## requiredModsSHA256
**Added in Version 1.0.**

Unused. Reserved for future use.

**Type**: `string[]`

**Default**: `[]`

## bannedModsSHA256
**Added in Version 1.0.**

Unused. Reserved for future use.

**Type**: `string[]`

**Default**: `[]`

## modPermissions
**Added in Version 1.1.**

Options to control what permissions server-side mods are granted.

### webRequests
**Added in Version 1.1.**

Allows server-side mods to make HTTP requests using the [[LuaScripting/HTTP.md]] table. When disabled, any calls to the `HTTP` table will be silently ignored.

**Type**: `boolean`

**Default**: `False`

## nonSyncedGameBehaviours
Options to enable various non-synced features on connected clients.

**Enabling these features will almost certainly cause issues or instability. Use at your own risk.**

### pedestrians
**Added in Version 1.0.**

Enables unsynced pedestrians for connected clients.

**Type**: `boolean`

**Default**: `False`

### traffic
**Added in Version 1.0.**

Enables unsynced traffic for connected clients.

**Type**: `boolean`

**Default**: `False`

### missions
**Added in Version 1.0.**

Enables unsynced missions traffic for connected clients.

**Type**: `boolean`

**Default**: `False`

### police
**Added in Version 1.0.**

Enables unsynced Hit & Runs for connected clients.

**Type**: `boolean`

**Default**: `False`

# Example Configuration File
Here is an example configuration file with all the default values

```yaml
serverName: My SHAR MP "Server"
password: ''
port: 7777
maxPlayers: 32
masterServer: 'https://launcher.donutteam.com'
masterServerAuthorisation: ''
broadcastServer: false
allowInGameTextChat: true
updateInterval: 60
updateIntervalLowBandwidth: 400
enableMods: true
serverModificationPaths: []
clientModificationPaths: []
requiredModNames: []
bannedModNames: []
requiredModsSHA256: []
bannedModsSHA256: []
modPermissions:
  webRequests: false
nonSyncedGameBehaviours:
  pedestrians: false
  traffic: false
  missions: false
  police: false
```
