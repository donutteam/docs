---
title: "SetDurationTime"
description: "Sets how long a timer objective should last."
authors: [ 2 ]
---

Sets how long a [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/timer.md]] should last.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetDurationTime( time );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetDurationTime( time )
```
{{ endtab }}
{{ endtabs }}

* **time**: The amount of seconds that the stage should last.
	* Unlike the base game command, decimal numbers are supported.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("timer");
		// This stage will complete after 5.5 seconds have passed.
		SetDurationTime(5.5);
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("timer")
		-- This stage will complete after 5.5 seconds have passed.
		Game.SetDurationTime(5.5)
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command replaces the base game's [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/SetDurationTime.md]].