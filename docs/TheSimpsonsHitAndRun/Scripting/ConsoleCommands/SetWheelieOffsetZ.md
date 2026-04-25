---
title: "SetWheelieOffsetZ"
description: "Sets the Z offset of the vehicle's center of mass when performing a wheelie."
authors: [ 104, 2 ]
---

This command sets the Z offset of the vehicle's center of mass when performing a wheelie.

In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetZ( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetZ( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the Z offset of the vehicle's center of mass when performing a wheelie.
    * Defaults to -1.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetZ(0.2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetZ(0.2)
```
{{ endtab }}
{{ endtabs }}

# Notes
See [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetWheelieOffsetX.md]] and [[SetWheelieOffsetY.md]] to set offsets for the other two axes.