---
title: "Multiplayer (Beta)"
description: "This hack makes the game have online multiplayer."
authors: [ 2, 1 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnMultiplayerPage.md }}

This hack makes the game have online multiplayer.

# Server Software
See [[/SimpsonsHitAndRunMultiplayerServer/Intro.md]].

# Settings
## Server
### Name
Set your ingame name.

### Name Colour
Set the color of your name ingame.

**Defaults to Yellow.**

### Host
The host to connect to.

**Defaults to 127.0.0.1.**

### Port
The port to connect to on the host.

**Defaults to 7777.**

### Server Password
The password for the server, if required.

### Low Bandwidth
Requests the server to send data at a lower rate.

**Defaults to Disabled.**

## Keybinds
### User Interface
* **Toggle Character Name Tags**: Toggles character name tags.
	* **Defaults to U.**
* **Toggle Vehicle Name Tags**: Toggles vehicle name tags.
	* **Defaults to I.**
* **View Player List**: Shows the player list when held.
	* **Defaults to X.**
* **Toggle Full Map**: Toggles a full screen map.
	* This map shows the positions of all players in the same level as you.
	* **Defaults to F10.**
* **Toggle Chat**: Toggles the chat box.
	* **Defaults to T.**

### Gameplay
* **Previous Character Model**: Swaps your character to the previous character model.
	* **Defaults to ..**
* **Next Character Model**: Swaps your character to the next character model.
	* **Defaults to /.**
* **Create Mission Radar Icon**: Places an icon on the radar.
	* **Defaults to Y.**
* **Spawn Explosion**: Spawns an explosion for all players in the same level with the **Mutators > Allow Explosions** setting enabled.
	* **Defaults to G.**

## Interface
### Name Tags
* **Players**: Shows name tags on players.
	* **Defaults to Enabled.**
* **Vehicles**: Shows name tags on vehicles.
	* **Defaults to Enabled.**

## Mutators
### Allow Explosions
Allows you to use the **Spawn Explosion** key and shows explosions from other players.

### Cops and Robbers
Makes certain cars driven by you and other players use a flashing chase car icon on the radar instead of the standard car icon.

The following cars are considered police cars by this mutator:
* Police Car (`wiggu_v`)
* Chase Sedan (`cSedan`)
* Hearse (`cHears`)
* `cPolice`

# Configuring This Hack
To configure this hack from a mod when its enabled, create a file named `Multiplayer.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>

<!--
	<DebugCharacter>
		Model: The internal name of the character model.
		AnimationSet: The animation set to use. Optional, defaults to npd.
-->

<Multiplayer>
	<!-- DebugCharacter without AnimationSet -->
	<DebugCharacter Name="maz" />

	<!-- DebugCharacter with AnimationSet -->
	<DebugCharacter Name="loren" AnimationSet="loren" />
</Multiplayer>
```

# Notes
This hack was previously distributed as part of separate "SHAR MP" builds of the Mod Launcher.

It also previously only had a single server, hosted by Donut Team, but this server has since been shuttered and users can now self-host their own server instead.
