---
title: "SetAllowSeatSlide"
description: "Sets whether or not the player is allowed to slide into the driver's seat from the passenger's seat."
authors: [ 104, 2 ]
---

This command sets whether or not the player is allowed to slide into the driver's seat from the passenger's seat.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetAllowSeatSlide( slide );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetAllowSeatSlide( slide )
```
{{ endtab }}
{{ endtabs }}

* **slide**: Whether seat sliding is allowed.
	* 0 is false, any non-0 value is true.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetAllowSeatSlide(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetAllowSeatSlide(1)
```
{{ endtab }}
{{ endtabs }}