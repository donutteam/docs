---
title: "SetObjFailDistance"
description: "Set the maximum distance the player can be from the stage vehicle dumping stuff in a dump objective that uses BindCollectibleTo."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Set the maximum distance the player can be from the stage vehicle in a [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/dump.md]] objective that uses [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/BindCollectibleTo.md]] to make the stage vehicle drop stuff near specific waypoints.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjFailDistance( fail_distance );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjFailDistance( fail_distance )
```
{{ endtab }}
{{ endtabs }}

* **fail_distance**: The maximum distance the player can be from the vehicle before they fail.
	* The default value without calling this command is 200.
	* Use 0 to disable failing the player regardless of distance.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("dump");
	SetObjTargetVehicle("snake_v");

	// Do not fail the player regardless of how far they get from snake_v
	SetObjFailDistance(0);

	AddCollectible("m5_collectible_1", "jeans");
	AddCollectible("m5_collectible_2", "molemanr");

	BindCollectibleTo(0, 0);
	BindCollectibleTo(1, 1);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("dump")
	Game.SetObjTargetVehicle("snake_v")

	-- Do not fail the player regardless of how far they get from snake_v
	Game.SetObjFailDistance(0)

	Game.AddCollectible("m5_collectible_1", "jeans")
	Game.AddCollectible("m5_collectible_2", "molemanr")

	Game.BindCollectibleTo(0, 0)
	Game.BindCollectibleTo(1, 1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}