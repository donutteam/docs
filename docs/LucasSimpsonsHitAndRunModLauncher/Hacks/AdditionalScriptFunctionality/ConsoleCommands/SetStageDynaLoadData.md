---
title: "SetStageDynaLoadData"
description: "Dumps all currently loaded regions and executes Dyna Load Data upon reaching a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Dumps all currently loaded regions and executes [[/TheSimpsonsHitAndRun/DynaLoadData.md]] upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageDynaLoadData( dyna_load_data, [interior_name] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageDynaLoadData( dyna_load_data, [interior_name] )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: A [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string that will be executed upon reaching the stage.
* **interior_name**: Sets the name of the currently loaded interior.
	* The P3D file for the interior should also be loaded in the **dyna_load_data** when this is provided.

# Examples
{{ tabs }}
{{ tab MFK }}
```js    
AddStage();
	// Load the L1 M7 power plant door upon reaching this stage
	SetStageDynaLoadData("l1m7door.p3d;");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua    
Game.AddStage()
	-- Load the L1 M7 power plant door upon reaching this stage
	Game.SetStageDynaLoadData("l1m7door.p3d;")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
If you only want to load new regions alongside what is currently loaded, use the [[AddStageDynaLoadData.md]] command instead.