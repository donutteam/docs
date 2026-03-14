---
title: "SetStageKickForce"
description: "Sets the kick force for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Sets the kick force for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageKickForce( kick_force );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageKickForce( kick_force )
```
{{ endtab }}
{{ endtabs }}

* **kick_force**: The amount of force the player's kicks should instill upon their victims for the stage.
	* The default force is **400.0**.
	* Negative values are supported.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Make the player able to send NPCs to the stratosphere for this stage
	SetStageKickForce(4000.0);

	AddObjective("dummy");
	CloseObjectve();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- Make the player able to send NPCs to the stratosphere for this stage
	Game.SetStageKickForce(4000.0);

	Game.AddObjective("dummy")
	Game.CloseObjectve()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}