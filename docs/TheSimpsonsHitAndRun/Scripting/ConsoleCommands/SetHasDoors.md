---
title: "SetHasDoors"
description: "This command sets whether or not a vehicle has doors."
authors: [ 104, 2 ]
---

This command sets whether or not a vehicle has doors.

This determines whether or not characters getting in to the vehicle do an animation of opening the door.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHasDoors( doors );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHasDoors( doors )
```
{{ endtab }}
{{ endtabs }}

* **doors**: Whether or not a vehicle has doors.
	* 0 is false, any non-0 value is true.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHasDoors(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHasDoors(1)
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is overridden by [[SetIrisTransition.md]] in the event that both are present.