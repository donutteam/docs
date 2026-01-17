---
title: "ActivateVehicle"
description: "Activates a vehicle previously added to a mission using AddStageVehicle."
authors: [ 2, 104 ]
---

Activates a vehicle previously added to a mission using [[AddStageVehicle.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ActivateVehicle( car, locator, behaviour, [driver] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ActivateVehicle( car, locator, behaviour, [driver] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to activate.
* **locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] to place the car on when activating it.
    * Radical always uses NULL for this argument, but the behaviour does work.
* **behaviour**: The type of [[/TheSimpsonsHitAndRun/VehicleBehaviours.md]] to give the car.
* **driver**: Set the driver of the vehicle.
	* This argument takes effect immediately, not when reaching the stage.
	* As a result, it's kind of useless and you should just use the 5th argument of [[AddStageVehicle.md]] instead probably.

# Examples

{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

	AddStage();
		// Add Skinner with NULL AI.
		AddStageVehicle("skinn_v", "m1_skinner_car", "NULL", "missions\\l1m0\\skinner.con", "skinner");

		AddObjective("dummy");
		CloseObjective();
	CloseStage();

	AddStage();
		// Then use ActivateVehicle to change him to chase AI in this stage.
		ActivateVehicle("skinn_v", "NULL", "chase");

		AddObjective("dummy");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	-- ...

	Game.AddStage()
		-- Add Skinner with NULL AI.
		Game.AddStageVehicle("skinn_v", "m1_skinner_car", "NULL", "missions\\l1m0\\skinner.con", "skinner")

		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()

	Game.AddStage()
		-- Then use ActivateVehicle to change him to chase AI in this stage.
		Game.ActivateVehicle("skinn_v","NULL","chase")

		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}