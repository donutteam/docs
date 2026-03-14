---
title: "IfAnyMissionCompleted"
description: "Checks if any of the given missions are completed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if any of the given missions are completed.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfAnyMissionCompleted( ...missions )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAnyMissionCompleted( ...missions )
```
{{ endtab }}
{{ endtabs }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/MissionCompletedArguments.md }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfAnyMissionCompleted("L7SR1", "L7SR2", "L7SR3")
{
	// Add extra stage when any of Level 7's street races have been completed
	AddStage();
		// ...
	CloseStage();
}
```
```js
IfAnyMissionCompleted("L1M1", "L1M2", "L1M3")
{
	// Only add this stage if the player has completed L1M1, L1M2 or L1M3
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfAnyMissionCompleted("L7SR1", "L7SR2", "L7SR3")

	-- Add extra stage when any of Level 7's street races have been completed
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
```lua
Game.IfAnyMissionCompleted("L1M1", "L1M2", "L1M3")

	-- Only add this stage if the player has completed L1M1, L1M2 or L1M3
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}