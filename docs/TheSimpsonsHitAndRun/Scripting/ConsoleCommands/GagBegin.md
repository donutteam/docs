---
title: "GagBegin"
description: "Begins a gag in a level."
authors: [ 2 ]
---

Begins a gag in a level.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoad.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
GagBegin( file_name );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagBegin( file_name )
```
{{ endtab }}
{{ endtabs }}

* **file_name**: The file name of the gag in the `art/nis/gags` folder.
	* This file name can be, at most, 12 characters including the required `.p3d` extension.

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
There is a maximum of 64 gags per level.