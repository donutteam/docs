---
title: "SetCharactersVisible"
description: "Sets the visibility of the driver and the passenger in a vehicle."
authors: [ 2, 104 ]
---

This command sets the visibility of the driver and the passenger in a vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCharactersVisible( visibility );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharactersVisible( visibility )
```
{{ endtab }}
{{ endtabs }}

* **visibility**: Whether the characters are visible.
	* 0 is false, any non-0 value is true.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCharactersVisible(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharactersVisible(1)
```
{{ endtab }}
{{ endtabs }}