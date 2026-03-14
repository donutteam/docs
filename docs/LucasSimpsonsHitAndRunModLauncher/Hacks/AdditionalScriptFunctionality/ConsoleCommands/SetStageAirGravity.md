---
title: "SetStageAirGravity"
description: "Sets the air gravity for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Sets the air gravity for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageAirGravity( air_gravity );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageAirGravity( air_gravity )
```
{{ endtab }}
{{ endtabs }}

* **air_gravity**: The air gravity to use for the stage.
	* The default air gravity is **-25.0**.
	* Values greater than or equal to 0 will be ignored because they break the game.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Half the gravity for this stage, idk some kind of low-grav platforming stage?
	SetStageAirGravity(-12.5);

	AddObjective("dummy");
	CloseObjectve();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- Half the gravity for this stage, idk some kind of low-grav platforming stage?
	Game.SetStageAirGravity(-12.5)

	Game.AddObjective("dummy")
	Game.CloseObjectve()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This only affects the player when they're on foot.