---
title: "IfRewardUnlocked"
description: "Checks if the player has unlocked a specific car or skin."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the player has unlocked a specific car or skin.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Any.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfRewardUnlocked( type, reward_name )
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfRewardUnlocked( type, reward_name )
```
{{ endtab }}
{{ endtabs }}

* **type**: The type of reward to check.
	* **1** / **skin**: Check for a `skin` reward.
	* **3** / **car**: Check for a `car` reward.
* **reward_name**: The name of the reward to check.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
IfRewardUnlocked("car", "elect_v")
{
	// Add an extra stage when the player has unlocked the electaurus
	AddStage();
		// ...
	CloseStage();
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfRewardUnlocked("car", "elect_v")

	-- Add an extra stage when the player has unlocked the electaurus
	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}