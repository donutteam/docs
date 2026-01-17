---
title: "SetIrisWipe"
description: "Sets up an iris wipe at the end of a stage."
authors: [ 2 ]
---

Sets up an iris wipe at the end of a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetIrisWipe( unused );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetIrisWipe( unused )
```
{{ endtab }}
{{ endtabs }}

* **unused**: Unused.
	* Despite being unused, this argument is **required**!

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// ...

	SetIrisWipe(0.1);
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- ...

	Game.SetIrisWipe(0.1)
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}