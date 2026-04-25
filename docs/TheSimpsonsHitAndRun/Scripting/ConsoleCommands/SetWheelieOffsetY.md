---
title: "SetWheelieOffsetY"
description: "Sets the Y offset of the vehicle's center of mass when performing a wheelie."
authors: [ 104, 2 ]
---

This command sets the Y offset of the vehicle's center of mass when performing a wheelie.

In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetY( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetY( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the Y offset of the vehicle's center of mass when performing a wheelie.
	* Defaults to 0.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetY(0.2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetY(0.2)
```
{{ endtab }}
{{ endtabs }}

# Notes
See [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetWheelieOffsetX.md]] and [[SetWheelieOffsetZ.md]] to set offsets for the other two axes.