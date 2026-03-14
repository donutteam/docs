---
title: "SetStageSlamForce"
description: "Sets the slam force for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Sets the slam force for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageSlamForce( slam_force );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageSlamForce( slam_force )
```
{{ endtab }}
{{ endtabs }}

* **slam_force**: The amount of force the player's slams should instill upon their victims for the stage.
	* The default force is **800.0**.
	* Negative values are supported.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Make the player able to send NPCs to the shadow realm for this stage
	SetStageSlamForce(8000.0);

	AddObjective("dummy");
	CloseObjectve();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- Make the player able to send NPCs to the shadow realm for this stage
	Game.SetStageSlamForce(8000.0);

	Game.AddObjective("dummy")
	Game.CloseObjectve()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}