---
title: "SetStageMusicEvent"
description: "Triggers a music event upon reaching a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Triggers a music event upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageMusicEvent( event );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageMusicEvent( event )
```
{{ endtab }}
{{ endtabs }}

* **event**: The name of a music event.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("dummy");
	CloseObjective();

	SetStageMusicEvent("M3_drama");
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("dummy")
	Game.CloseObjective()

	Game.SetStageMusicEvent("M3_drama")
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is similar to the [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/StageStartMusicEvent.md]] in the base game, except the underlying code for triggering the event is different and can trigger *any* music event instead of a limited subset.