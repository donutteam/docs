---
title: "SetStagePedGroup"
description: "Set the active ped group upon reaching a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Set the active ped group upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStagePedGroup( group_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStagePedGroup( group_index )
```
{{ endtab }}
{{ endtabs }}

* **group_index**: The index of the ped group to switch to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Switch to ped group 2 when reaching this stage.
	SetStagePedGroup(2);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()	
	-- Switch to ped group 2 when reaching this stage.
	Game.SetStagePedGroup(2)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This will persist until the player enters a [[/Pure3DFiles/ChunkTypes/TriggerVolume.md]] inside a [[/Pure3DFiles/ChunkTypes/Locator.md|PedGroup Locator]], a subsequent stage calls the command again or the player mission selects to a mission that calls [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/UsePedGroup.md]].