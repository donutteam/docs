---
title: "SetMaxTraffic"
description: "Sets the maximum number of traffic cars that will appear in a stage."
authors: [ 2116 ]
---

Sets the maximum number of traffic cars that will appear in a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMaxTraffic( cars );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMaxTraffic( cars ) 
```
{{ endtab }}
{{ endtabs }}

* **cars**: The number of cars that will appear in the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Only 2 cars will appear in this stage.
	SetMaxTraffic(2);
		
	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- Only 2 cars will appear in this stage.
	Game.SetMaxTraffic(2)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
The traffic car limit will persist until the level is reloaded, or this command is called again.

As such, it is a good idea to call it at the start of every mission.