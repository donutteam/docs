---
title: "GagSetSparkle"
description: "Sets if a gag should sparkle."
authors: [ 2 ]
---

Sets if a gag should sparkle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoadGag.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
GagSetSparkle( sparkle );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagSetSparkle( sparkle )
```
{{ endtab }}
{{ endtabs }}

* **sparkle**: Whether the gag will sparkle. 0 or 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_bbq.p3d");
	// ...
	GagSetSparkle(1);
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_bbq.p3d")
	-- ...
	Game.GagSetSparkle(1)
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Notes
If the gag is set to be persistent with [[GagSetPersist.md]] and has already been completed, sparkles will be forcefully disabled.