---
title: "IfAllCheatsEnabled"
description: "Checks if all of the given cheats are enabled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if all of the given cheats are enabled.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfAllCheatsEnabled( ...cheats )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAllCheatsEnabled( ...cheats )
```
{{ endtab }}
{{ endtabs }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/CheatEnabledArguments.md }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js    
AddStage();
	IfAllCheatsEnabled("InvincibleCar", "HighAcceleration")
	{
		// do something differently for this stage if the user is a filthy cheater
		//	in all of these specific ways
	}

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.IfAllCheatsEnabled("InvincibleCar", "HighAcceleration")
	
		-- do something differently for this stage if the user is a filthy cheater
		--	in all of these specific ways
	Game.EndIf()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
* {{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/CheatTable.md }}