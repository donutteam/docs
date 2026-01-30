---
title: "SetDriver"
description: "Sets the driver of a vehicle."
authors: [ 2 ]
---

This command sets the driver of a vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetDriver( character );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetDriver( character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character who will drive the vehicle.
	* This character will only appear if they're not suppressed with [[SuppressDriver.md]] in the level's load script.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// This vehicle will have Homer as its driver (unless he's suppressed for the level)
SetDriver("homer");
```
```js
// "none" is special and means the vehicle will have no driver.
SetDriver("none");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- This vehicle will have Homer as its driver (unless he's suppressed for the level)
Game.SetDriver("homer")
```
```lua
-- "none" is special and means the vehicle will have no driver.
Game.SetDriver("none")
```
{{ endtab }}
{{ endtabs }}

# Notes
Using "none" is **NOT** equivalent to not calling the command outright. Omitting the command entirely is special in two cases:
* **Traffic Vehicles**: Traffic car CON files do not call this command at all. This indicates to the game that it should add an invisible driver that uses random traffic dialogue.
* **Mission Vehicles**: Mission vehicles added with [[AddStageVehicle.md]] can define a path to their CON file. These CON files typically omit SetDriver as [[AddStageVehicle.md]] can specify a driver inline which does not work if the CON file does so.
