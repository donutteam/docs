---
title: "InitLevelPlayerVehicle"
description: "Initialises a player vehicle for a level or a forced car mission."
authors: [ 2, 735 ]
---

Initialises a player vehicle for a level or a forced car mission.

# Scope
## Using "DEFAULT" Slot
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

## Using "OTHER" Slot
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
InitLevelPlayerVehicle( vehicle_name, locator_name, slot, [con_file] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.InitLevelPlayerVehicle( vehicle_name, locator_name, slot, [con_file] )
```
{{ endtab }}
{{ endtabs }}

* **vehicle_name**: The name of the vehicle to use.
* **locator_name**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] to spawn the vehicle at.
* **slot**: The slot to put the vehicle in.
	* **DEFAULT**: Use this vehicle as the level's default car.
	* **OTHER**: Use this vehicle as a forced car in a mission.
* **con_file**: A path to a CON file.
	* Optional, defaults to the car's normal CON file in `scripts/cars`.

# Examples
## Level Default Car

## Mission Forced Car
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m3");
	// ...

	// This sets Comic Book Guy's vehicle as the starting vehicle for this mission.
	InitLevelPlayerVehicle("comic_v", "m3_cbgcar_sd", "OTHER");
	
	SetForcedCar();
	
	AddStage();
		// ...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m3")
	-- ...

	-- This sets Comic Book Guy's vehicle as the starting vehicle for this mission.
	Game.InitLevelPlayerVehicle("comic_v", "m3_cbgcar_sd", "OTHER")
	
	Game.SetForcedCar()
	
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}