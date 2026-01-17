---
title: "AddStageVehicle"
description: "Adds a vehicle to a stage in a mission."
authors: [ 2 ]
---

Adds a vehicle to a stage in a mission.

# Context
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageVehicle( car, locator, behaviour, [con_file, driver] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageVehicle( car, locator, behaviour, [con_file, driver] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to add.
* **locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] to place the car on.
* **behaviour**: The type of [[/TheSimpsonsHitAndRun/VehicleBehaviours.md|Vehicle Behaviour]] to give the car.
* **con_file**: The CON file to use on the car.
    * Optional, defaults to the car's CON file in the `scripts\cars` folder if omitted.
* **driver**: The driver of the vehicle. This only works if the **con_file** does not call [[SetDriver.md]].
    * Optional, defaults to no driver if omitted (unless the specified **con_file** sets a driver).

# Examples
## Activate Immediately
This example adds Skinner's car and activates it immediately with chase AI.
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Add Skinner with chase AI right away
	AddStageVehicle("skinn_v", "m1_skinner_car", "chase", "missions\\l1m0\\skinner.con", "skinner");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- Add Skinner with chase AI right away
	Game.AddStageVehicle("skinn_v", "m1_skinner_car", "chase", "missions\\l1m0\\skinner.con", "skinner")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

## Activate Later
This example adds Skinner's car with no AI and then activates it in the following stage with [[ActivateVehicle.md]].

{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Add Skinner with no AI
	AddStageVehicle("skinn_v", "m1_skinner_car", "NULL", "missions\\l1m0\\skinner.con", "skinner");

	AddObjective("dummy");
	CloseObjective();
CloseStage();

AddStage();
	// Then use ActivateVehicle in the next stage to activate him
	ActivateVehicle("skinn_v","NULL","chase");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua	Game.AddStage()
Game.AddStage()
	-- Add Skinner with no AI
	Game.AddStageVehicle("skinn_v", "m1_skinner_car", "NULL", "missions\\l1m0\\skinner.con", "skinner")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()

Game.AddStage()
	-- Then use ActivateVehicle in the next stage to activate him
	Game.ActivateVehicle("skinn_v", "NULL", "chase")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}