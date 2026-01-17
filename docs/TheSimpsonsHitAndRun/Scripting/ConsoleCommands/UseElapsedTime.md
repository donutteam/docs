---
title: "UseElapsedTime"
description: "Makes the stage timer count up rather than down."
authors: [ 2 ]
---

Makes the stage timer count up rather than down.

The stage should also call [[SetStageTime.md]] or [[AddStageTime.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
UseElapsedTime();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.UseElapsedTime()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageTime(0);
	UseElapsedTime(); // Make the timer count up from 0 in this stage

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageTime(0)
	Game.UseElapsedTime() -- Make the timer count up from 0 in this stage

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
In the base game, this command is only used in wager races.

It can be used outside of that context but the timer will flash red when it is below 10 seconds.