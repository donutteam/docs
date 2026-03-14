---
title: "SetStageEnabledCheats"
description: "Sets the specified cheats to enabled for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Sets the specified cheats to enabled for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageEnabledCheats( ...cheats );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageEnabledCheats( ...cheats )
```
{{ endtab }}
{{ endtabs }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/CheatEnabledArguments.md }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Let the player go absolutely HAM on traffic cars for this stage with no consequences
	SetStageEnabledCheats("InvincibleCar", "OneTapTrafficDeath");

	AddObjective("dummy");
	CloseObjectve();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- Let the player go absolutely HAM on traffic cars for this stage with no consequences
	Game.SetStageEnabledCheats("InvincibleCar", "OneTapTrafficDeath")

	Game.AddObjective("dummy")
	Game.CloseObjectve()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/CheatTable.md }}