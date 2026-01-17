---
title: "AddSpawnPoint"
description: "Adds a spawn point for a Wasp Camera to a level using a XYZ position."
authors: [ 2 ]
---

Adds a spawn point for a Wasp Camera to a level using a XYZ position.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddSpawnPointByLocatorScript( spawn_point_name, state_prop_name, unused_instance_name, x, y, z, radius, unused_timeout );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddSpawnPointByLocatorScript( spawn_point_name, state_prop_name, unused_instance_name, x, y, z, radius, unused_timeout )
```
{{ endtab }}
{{ endtabs }}

* **spawn_point_name**: The name of this spawn point. Should be unique.
* **state_prop_name**: The name of the state prop to use.
	* Typically, `beecamera`.
* **unused_instance_name**: Unused.
* **x**: The X position.
* **y**: The Y position.
* **z**: The Z position.
* **radius**: The radius of the spawn point's sphere trigger.
* **unused_timeout**: Unused.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level01/leveli.mfk
AddSpawnPoint("SimpsonsHouse", "beecamera", "Shelly", "222.041", "4.5", "-169.169", "50.0", "20");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level01/leveli.mfk
Game.AddSpawnPoint("SimpsonsHouse", "beecamera", "Shelly", "222.041", "4.5", "-169.169", "50.0", "20")
```
{{ endtab }}
{{ endtabs }}

# Notes
Radical never actually uses this command, with all references to it being commented out, instead opting for [[AddSpawnPointByLocatorScript.md]].