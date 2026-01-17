---
title: "SetFadeOut"
description: "Sets up a fade to black at the end of a stage."
authors: [ 2 ]
---

Sets up a fade to black at the end of a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetFadeOut( unused );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetFadeOut( unused )
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

	SetFadeOut(0.1);
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	-- ...

	Game.SetFadeOut(0.1)
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}