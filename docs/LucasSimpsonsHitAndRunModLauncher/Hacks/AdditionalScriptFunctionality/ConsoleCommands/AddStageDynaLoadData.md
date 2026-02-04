---
title: "AddStageDynaLoadData"
description: "Executes Dyna Load Data upon reaching a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Executes [[/TheSimpsonsHitAndRun/DynaLoadData.md]] upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageDynaLoadData( dyna_load_data, [interior_name] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageDynaLoadData( dyna_load_data, [interior_name] )
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
	AddStageDynaLoadData("l1m7door.p3d;");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua    
Game.AddStage()
	-- Load the L1 M7 power plant door upon reaching this stage
	Game.AddStageDynaLoadData("l1m7door.p3d;")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
If you wish to unload everything currently loaded before loading new regions for the stage, use the [[SetStageDynaLoadData.md]] command instead.