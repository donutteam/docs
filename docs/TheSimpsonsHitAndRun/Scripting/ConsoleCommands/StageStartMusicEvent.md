---
title: "StageStartMusicEvent"
description: "Triggers a mission music event upon reaching a stage."
authors: [ 2 ]
---

Triggers a mission music event upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
StageStartMusicEvent( event );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.StageStartMusicEvent( event )
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

	StageStartMusicEvent("M3_drama");
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("dummy")
	Game.CloseObjective()

	Game.StageStartMusicEvent("M3_drama")
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command causes the game to trigger the `CHANGE_MUSIC` [[/TheSimpsonsHitAndRun/Events.md|Event]], which itself can only actually trigger a limited subset of all available music events.

Substituting "X" for a number from 0 to 7, this command can trigger the following events:
* MX_start
* MX_drama
* MX_win
* MX_lose
* MX_get_out_of_car
* MX_10sec_to_go

As well as these events:
* Bonus_start
* Bonus_drama
* Bonus_win
* Bonus_lose
* Bonus_get_out_of_car
* Bonus_10sec_to_go

For a command that can trigger *any* music event, use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetStageMusicEvent.md]] command provided by the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/Intro.md|Additional Script Functionality]] hack.