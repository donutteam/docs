---
title: "IfCurrentSkin"
description: "Checks if the player's current skin is one of the given skins."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the player's current skin is one of the given skins.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentSkin( ...skins )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentSkin( ...skins )
```
{{ endtab }}
{{ endtabs }}

* **...skins**: List up to 15 skin names to check as separate arguments.
	* Skin names are case-insensitive.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentSkin("h_fat")
{
	// Add an extra stage to the mission if the player started the mission with fat-ass Homer
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentSkin("h_fat")

	-- Add an extra stage to the mission if the player started the mission with fat-ass Homer
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}