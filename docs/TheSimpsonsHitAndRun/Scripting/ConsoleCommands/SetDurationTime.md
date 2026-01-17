---
title: "SetDurationTime"
description: "Sets how long a timer objective should last."
authors: [ 2, 735, 27739 ]
---

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

* **time**: The duration (in seconds) that the stage should last.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("timer");
		// This stage will complete after 5 seconds have passed.
		SetDurationTime(5);
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("timer")
		-- This stage will complete after 5 seconds have passed.
		Game.SetDurationTime(5)
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
Mods can use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/Intro.md]] hack to replace this command with one that supports decimal numbers.

See [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetDurationTime.md]] for details on that hack's implementation.
