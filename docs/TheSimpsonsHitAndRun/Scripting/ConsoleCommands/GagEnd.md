---
title: "GagEnd"
description: "Ends a gag in a level."
authors: [ 2 ]
---

Ends a gag in a level.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoad.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_s5.p3d");
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_s5.p3d")
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Notes
If this gag is the Itchy & Scratchy movie ticket, the game will remove the gag from the level if it has already been obtained.