---
title: "AddTrafficModel"
description: "Adds a vehicle to a traffic group."
authors: [ 104 ]
---

This command adds a vehicle to a traffic group.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInitTrafficGroup.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddTrafficModel( car, amount, [no_park] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddTrafficModel( car, amount, [no_park] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to add.
* **amount**: How many instances of the car can appear at once.
* **no_park**: Prevent the vehicle from spawning idle on [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locators]] with the Parked Car flag.
    * Optional, defaults to 0 (which allows it to be parked).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
CreateTrafficGroup(0);
	AddTrafficModel("minivanA", 2); 	// 2 instances, can appear parked
	AddTrafficModel("glastruc", 1, 1); 	// 1 instance, cannot appear parked
	AddTrafficModel("schoolbu", 1, 1);
	AddTrafficModel("pickupA", 1);
CloseTrafficGroup();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CreateTrafficGroup(0)
	Game.AddTrafficModel("minivanA", 2) 	-- 2 instances, can appear parked
	Game.AddTrafficModel("glastruc", 1, 1)	-- 1 instance, cannot appear parked
	Game.AddTrafficModel("schoolbu", 1, 1)
	Game.AddTrafficModel("pickupA", 1)
Game.CloseTrafficGroup()
```
{{ endtab }}
{{ endtabs }}

# Notes
By default, the combined total of all the **amount** values for each call to this command must amount to 5 or the game will crash.

You can have more or less using the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomTrafficSupport.md]] hack.