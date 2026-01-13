---
title: "GagSetInterior"
description: "Sets the interior for a gag in a level."
authors: [ 2 ]
---

Sets the interior for a gag in a level.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoadGag.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
GagSetInterior( interior_name );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagSetInterior( interior_name )
```
{{ endtab }}
{{ endtabs }}

* **interior_name**: The name of an interior.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_sqsh.p3d");
	// ...
	GagSetInterior("KwikEMart");
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_sqsh.p3d")
	-- ...
	Game.GagSetInterior("KwikEMart")
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Notes
If [[GagSetPosition.md]] is not also called with a locator name in the gag, calling this command will set the gag to be positioned at the interior's `InteriorOrigin` locator.