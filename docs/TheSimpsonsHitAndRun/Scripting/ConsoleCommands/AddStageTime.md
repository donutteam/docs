---
title: "AddStageTime"
description: "Adds more time to the timer upon reaching a stage."
authors: [ 2, 735 ]
---

Adds more time to the timer upon reaching a stage.

# Context
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageTime( time );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageTime( time )
```
{{ endtab }}
{{ endtabs }}

* **time**: The amount of time, in seconds, to add to the active stage timer.
	* The game adds 1 to whatever value you specify here, meaning 0 will actually result in the game adding 1 second.
	* If this quirk bothers you, you can instead use -1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

	AddStage();
		// Set the stage timer to 60 seconds here.
		SetStageTime(60);
		
		AddObjective("dummy");
		CloseObjective();
	
	CloseStage();
	
	AddStage();
		// Then add 30 seconds to the stage timer when reaching this stage.
		AddStageTime(30);
	
		AddObjective("dummy");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	-- ...

	Game.AddStage()
		-- Set the stage timer to 60 seconds here.
		Game.SetStageTime(60)
		
		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()
	
	Game.AddStage()
		-- Then add 30 seconds to the stage timer when reaching this stage.
		Game.AddStageTime(30)
	
		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
* In order to actually fail the player when they run out of time in a stage, you must also add a [[../MissionConditions/timeout.md]] condition in the stage.
* If there was no stage timer prior to reaching the stage, then this commands functions basically the same as [[SetStageTime.md]].