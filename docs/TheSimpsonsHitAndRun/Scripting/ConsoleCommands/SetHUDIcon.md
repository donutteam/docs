---
title: "SetHUDIcon"
description: "Sets the HUD icon sprite to display during a stage."
authors: [ 2, 735 ]
---

Sets the HUD icon sprite to display during a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHUDIcon( sprite_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHUDIcon( sprite_name )
```
{{ endtab }}
{{ endtabs }}

* **sprite_name**: The name of the HUD icon sprite to use.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m3");
	AddStage();
		SetHUDIcon("simpsons");

		AddObjective("dummy");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m3")
	Game.AddStage()
		Game.SetHUDIcon("simpsons")

		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}