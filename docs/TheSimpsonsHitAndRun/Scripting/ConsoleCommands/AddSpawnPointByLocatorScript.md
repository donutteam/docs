---
title: "AddSpawnPointByLocatorScript"
description: "Adds a spawn point for a Wasp Camera to a level using a locator."
authors: [ 2 ]
---

Adds a spawn point for a Wasp Camera to a level using a locator.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddSpawnPointByLocatorScript( spawn_point_name, state_prop_name, unused_instance_name, locator_name, radius, unused_timeout );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddSpawnPointByLocatorScript( spawn_point_name, state_prop_name, unused_instance_name, locator_name, radius, unused_timeout )
```
{{ endtab }}
{{ endtabs }}

* **spawn_point_name**: The name of this spawn point. Should be unique.
* **state_prop_name**: The name of the state prop to use.
	* Typically, `beecamera`.
* **unused_instance_name**: Unused.
* **locator_name**: The name of a [[/Pure3DFiles/ChunkTypes/Locator.md|Generic Locator]].
* **radius**: The radius of the spawn point's sphere trigger.
* **unused_timeout**: Unused.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level01/leveli.mfk
AddSpawnPointByLocatorScript("w_lemon", "beecamera", "Shelley", "w_lemon", "15.0", "60");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level01/leveli.mfk
Game.AddSpawnPointByLocatorScript("w_lemon", "beecamera", "Shelley", "w_lemon", "15.0", "60")
```
{{ endtab }}
{{ endtabs }}