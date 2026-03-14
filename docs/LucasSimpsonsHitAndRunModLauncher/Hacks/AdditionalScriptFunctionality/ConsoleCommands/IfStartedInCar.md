---
title: "IfStartedInCar"
description: "Checks if the player started a mission in a car."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the player started a mission in a car.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfStartedInCar()
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfStartedInCar()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfStartedInCar()
{
	// Add an extra stage when the player started the mission in a car
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfStartedInCar()

	-- Add an extra stage when the player started the mission in a car
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}