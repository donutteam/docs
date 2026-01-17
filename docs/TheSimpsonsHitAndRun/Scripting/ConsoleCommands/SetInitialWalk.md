---
title: "SetInitialWalk"
description: "Sets a CarStart locator that the player character will automatically walk towards when the mission is selected or restarted."
authors: [ 2116 ]
---

Sets a [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the player character will automatically walk towards when the mission is selected or restarted.

# Context
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetInitialWalk( walk_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetInitialWalk( walk_locator )
```
{{ endtab }}
{{ endtabs }}

* **walk_locator**: The [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the player will walk to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...
	
	SetInitialWalk("level1_homer_walkto");
	
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
	
	Game.SetInitialWalk("level1_homer_walkto")
	
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}