---
title: "SetStageTime"
description: "Sets the time on the timer upon reaching a stage."
authors: [ 2, 735 ]
---

Sets the time on the timer upon reaching a stage.

# Context
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageTime( time );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageTime( time )
```
{{ endtab }}
{{ endtabs }}

* **time**: The amount of time, in seconds, to set the stage timer to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

	AddStage();
		SetStageTime(60);	
	
		AddObjective("dummy");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1");
	-- ...

	Game.AddStage();
		Game.SetStageTime(60);
	
		Game.AddObjective("dummy");
		Game.CloseObjective();
	Game.CloseStage();
Game.CloseMission();
```
{{ endtab }}
{{ endtabs }}

# Notes
* In order to actually fail the player when they run out of time in a stage, you must also add a [[../MissionConditions/timeout.md]] condition in the stage.
* To add time to whatever the player had left from a previous stage, use [[AddStageTime.md]] instead.