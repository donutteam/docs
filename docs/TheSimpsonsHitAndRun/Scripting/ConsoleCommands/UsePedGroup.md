---
title: "UsePedGroup"
description: "Set what ped group will be used when the mission is selected or restarted."
authors: [ 2, 2116 ]
---

Set what ped group will be used when the mission is selected or restarted.

# Context
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
UsePedGroup( group_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.UsePedGroup( group_index )
```
{{ endtab }}
{{ endtabs }}

* **group_index**: The index of the ped group.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...
	
	// Use the 2nd ped group when restarting the mission.
	// This does NOT apply when going from the SD mission into the main mission.
	UsePedGroup(2);

	AddStage();	
		// ...		
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	// ...
	
	-- Use the 2nd ped group when restarting the mission.
	-- This does NOT apply when going from the SD mission into the main mission.
	Game.UsePedGroup(2)

	Game.AddStage()	
		// ...		
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}