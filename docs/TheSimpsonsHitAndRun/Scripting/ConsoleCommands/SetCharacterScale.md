---
title: "SetCharacterScale"
description: "Sets the scale of the driver and the passenger in a vehicle."
authors: [ 2 ]
---

This command sets the scale of the driver and the passenger in a vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCharacterScale( scale );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharacterScale( scale )
```
{{ endtab }}
{{ endtabs }}

* **scale**: The scale of the characters.
    * Defaults to 1.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCharacterScale(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharacterScale(1)
```
{{ endtab }}
{{ endtabs }}