---
title: "IfAnyCheatEnabled"
description: "Checks if any of the given cheats are enabled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if any of the given cheats are enabled.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfAnyCheatEnabled( ...cheats )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAnyCheatEnabled( ...cheats )
```
{{ endtab }}
{{ endtabs }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/IfAnyAllCheatArguments.md }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js    
AddStage();
	IfAnyCheatEnabled("InvincibleCar", "HighAcceleration")
	{
		// do something differently for this stage if the user is a filthy cheater
		//	in any of these specific ways
	}

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua    
Game.AddStage()
	Game.IfAnyCheatEnabled("InvincibleCar", "HighAcceleration")
	
		-- do something differently for this stage if the user is a filthy cheater
		--	in any of these specific ways
	Game.EndIf()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
Lua scripts can also use the global [[../../CustomFiles/LuaTables/Cheat.md]] table in place of the bit flags or strings, for convenience.