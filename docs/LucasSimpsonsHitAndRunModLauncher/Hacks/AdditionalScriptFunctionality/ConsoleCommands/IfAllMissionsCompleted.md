---
title: "IfAllMissionsCompleted"
description: "Checks if all of the given missions are completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if all of the given missions are completed.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfAllMissionsCompleted( ...missions )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAllMissionsCompleted( ...missions )
```
{{ endtab }}
{{ endtabs }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/MissionCompletedArguments.md }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfAllMissionsCompleted("L7SR1", "L7SR2", "L7SR3")
{
	// Add extra stage when all of Level 7's street races have been completed
	AddStage();
		// ...
	CloseStage();
}
```
```js
!IfAllMissionsCompleted("L1M1", "L1M2", "L1M3")
{
	// Only add this stage if the player hasn't completed L1M1 to L1M3
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAllMissionsCompleted("L7SR1", "L7SR2", "L7SR3")

	-- Add extra stage when all of Level 7's street races have been completed
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
```lua
Game.Not_IfAllMissionsCompleted("L1M1", "L1M2", "L1M3")

	-- Only add this stage if the player hasn't completed L1M1 to L1M3
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}