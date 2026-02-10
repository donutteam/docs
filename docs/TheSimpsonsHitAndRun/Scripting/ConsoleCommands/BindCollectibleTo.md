---
title: "BindCollectibleTo"
description: "Binds a collectible in a dump objective to a waypoint."
authors: [ 2 ]
---

This command binds a collectible in a [[../MissionObjectives/dump.md]] objective to a waypoint.

Calling this command disables the player's ability to knock collectibles out of the car by slamming into it, so all collectibles in the stage **must** be bound to waypoints.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
BindCollectibleTo( collectible_index, waypoint_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.BindCollectibleTo( collectible_index, waypoint_index )
```
{{ endtab }}
{{ endtabs }}

* **collectible_index**: The 0-based index of the collectible.
* **waypoint_index**: The 0-based index of the waypoint to bind the collectible to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStageWaypoint("m5_AI_path_4");
AddStageWaypoint("m5_AI_path_7");
AddStageWaypoint("m5_AI_path_10");
AddStageWaypoint("m5_AI_path_16");

AddObjective("dump");
	SetObjTargetVehicle("snake_v");
	AddCollectible("m5_collectible_1", "jeans");
	AddCollectible("m5_collectible_2", "molemanr");
	AddCollectible("m5_collectible_3", "h_soda");
	BindCollectibleTo(0, 0); // jeans will drop when snake_v gets near m5_AI_path_4
	BindCollectibleTo(1, 1); // molemanr will drop when snake_v gets near m5_AI_path_7
	BindCollectibleTo(2, 2); // h_soda will drop when snake_v gets near m5_AI_path_10
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageWaypoint("m5_AI_path_4")
Game.AddStageWaypoint("m5_AI_path_7")
Game.AddStageWaypoint("m5_AI_path_10")
Game.AddStageWaypoint("m5_AI_path_16")

Game.AddObjective("dump")
	Game.SetObjTargetVehicle("snake_v")
	Game.AddCollectible("m5_collectible_1", "jeans")
	Game.AddCollectible("m5_collectible_2", "molemanr")
	Game.AddCollectible("m5_collectible_3", "h_soda")
	Game.BindCollectibleTo(0, 0) -- jeans will drop when snake_v gets near m5_AI_path_4
	Game.BindCollectibleTo(1, 1) -- molemanr will drop when snake_v gets near m5_AI_path_7
	Game.BindCollectibleTo(2, 2) -- h_soda will drop when snake_v gets near m5_AI_path_10
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}