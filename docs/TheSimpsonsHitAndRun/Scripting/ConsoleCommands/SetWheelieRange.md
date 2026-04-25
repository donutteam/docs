---
title: "SetWheelieRange"
description: "Sets the distance for which a vehicle will perform a wheelie when accelerating."
authors: [ 104, 2 ]
---

This command sets the distance for which a vehicle will perform a wheelie when accelerating.

In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieRange( range );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieRange( range )
```
{{ endtab }}
{{ endtabs }}

* **range**: Sets the distance for which a vehicle will perform a wheelie.
	* Defaults to 0.0.
	* When in this state, the vehicles's center of mass is offset to the values specified in [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetWheelieOffsetX.md]], [[SetWheelieOffsetY.md]] and [[SetWheelieOffsetZ.md]].

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieRange(0.3);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieRange(0.3)
```
{{ endtab }}
{{ endtabs }}