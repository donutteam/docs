---
title: "IfCurrentLevel"
description: "Checks if the player is in one of the given levels."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the player is in one of the given levels.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentLevel( ...levels )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentLevel( ...levels )
```
{{ endtab }}
{{ endtabs }}

* **...levels**: List up to 15 level numbers to check.

# Examples
{{ tabs }}
{{ tab CON }}
```js
!IfCurrentLevel(4, 5, 6, 7)
{
	// Base Speed
	SetTopSpeed(120.0);
}

IfCurrentLevel(4, 5, 6, 7)
{
	// Boost the top speed in later levels of the game!
	SetTopSpeed(160.0);
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.Not_IfCurrentLevel(4, 5, 6, 7)

	-- Base Speed
	Game.SetTopSpeed(120.0)
Game.EndIf()

Game.IfCurrentLevel(4, 5, 6, 7)

	-- Boost the top speed in later levels of the game!
	Game.SetTopSpeed(160.0)
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
* {{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}
* This commands supports up to 15 arguments because that's the maximum amount of arguments an ASF command can take and there's no particularly compelling reason for it not to.
* The example given uses this in a CON file because those scripts can be executed on any level, but you can technically use it anywhere.