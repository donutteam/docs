---
title: "DisableTrigger"
description: "Disable a locator's trigger(s) for a stage. Repeat for each locator's triggers you'd like to disable."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Disable a locator's trigger(s) for a stage. Repeat for each locator's triggers you'd like to disable.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
DisableTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.DisableTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of a locator whose triggers will be disabled.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	DisableTrigger("z2phone1");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.DisableTrigger("z2phone1")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Version History
## Version 1.22.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/AdditionalScriptFunctionality/ConsoleCommands/DisableTrigger.md }}