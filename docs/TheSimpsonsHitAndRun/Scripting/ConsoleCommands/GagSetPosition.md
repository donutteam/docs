---
title: "GagSetPosition"
description: "Sets the position of a gag in a level."
authors: [ 2 ]
---

Sets the position of a gag in a level.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoadGag.md }}

# Syntax
## Using a Locator (1 Argument)
{{ tabs }}
{{ tab MFK }}
```js
GagSetPosition( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagSetPosition( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of a locator.

## Using a Position (3 Arguments)
{{ tabs }}
{{ tab MFK }}
```js
GagSetPosition( x, y, z );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagSetPosition( x, y, z )
```
{{ endtab }}
{{ endtabs }}

* **x**: The X position.
* **y**: The Y position.
* **z**: The Z position.

# Examples
## Using a Locator (1 Argument)
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_sqsh.p3d");
	// ...
	GagSetPosition("Squish");
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_sqsh.p3d")
	-- ...
	Game.GagSetPosition("Squish")
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

## Using a Position (3 Arguments)
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_bbq.p3d");
	// ...
	GagSetPosition(10, 10, 10);
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_bbq.p3d")
	-- ...
	Game.GagSetPosition(10, 10, 10)
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Notes
If the gag is added to an interior via [[GagSetInterior.md]], a locator must be used or the gag's position will be ignored and set to the position of the interior's `InteriorOrigin` locator.