---
title: "IfCurrentCar"
description: "Checks if the player's current car is one of the given cars."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the player's current car is one of the given cars.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentCar( ...cars )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentCar( ...cars )
```
{{ endtab }}
{{ endtabs }}

* **...cars**: List up to 15 car names to check as separate arguments.
	* Car names are case-insensitive.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentCar("famil_v", "honor_v")
{
	// Add an extra stage when the player started the mission
	// 	in the Family Sedan or Honor Roller
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentCar("famil_v", "honor_v")

	-- Add an extra stage when the player started the mission
	-- 	in the Family Sedan or Honor Roller
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}