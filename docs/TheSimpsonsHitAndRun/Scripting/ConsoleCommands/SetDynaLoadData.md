---
title: "SetDynaLoadData"
description: "Sets a Dyna Load Data string to be executed when restarting a mission."
authors: [ 2, 2116 ]
---

Sets a Dyna Load Data string to be executed when restarting a mission.

# Context
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetDynaLoadData( dyna_load_data );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetDynaLoadData( dyna_load_data )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: A [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string that will be executed when the mission loads.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...
	
	SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;");

	AddStage();	
		// ...	
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	-- ...
	
	Game.SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

	Game.AddStage() 	
		-- ...	
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
At least one zone must be loaded, otherwise the game will hang on the loading screen.

Specifiying a blank string like `SetDynaLoadData("");` will crash the game.