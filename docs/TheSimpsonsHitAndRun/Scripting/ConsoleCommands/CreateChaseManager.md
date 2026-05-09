---
title: "CreateChaseManager"
description: "Creates a chase manager for a level."
authors: [ 2 ]
---

Creates a chase manager for a level.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CreateChaseManager( car_name, con_file, spawn_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CreateChaseManager( car_name, con_file, spawn_rate )
```
{{ endtab }}
{{ endtabs }}

* **car_name**: The chase car to spawn.
* **con_file**: The CON file to use for the chase cars.
	* Relative to `scripts/cars`.
* **spawn_rate**: The spawn rate of this chase managers cars.
	* This technically sets a value and has an effect on spawning logic in the game, but as a consequence of there being a max of 1 chase manager, effectively does nothing meaningful.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level01/leveli.mfk
CreateChaseManager("cPolice", "Pursuit\L1cop.con", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level01/leveli.mfk
Game.CreateChaseManager("cPolice", "Pursuit\\L1cop.con", 1);
```
{{ endtab }}
{{ endtabs }}

# Notes
There is a max of 1 chase manager per level.