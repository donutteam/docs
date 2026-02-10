---
title: "GagSetPersist"
description: "Sets if a gag counts towards the level's gags total."
authors: [ 2 ]
---

Sets if a gag counts towards the level's gags total.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoadGag.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
GagSetPersist( persist );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.GagSetPersist( persist );
```
{{ endtab }}
{{ endtabs }}

* **persist**: Whether the gag will count towards the level's gags total. 0 or 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
GagBegin("gag_sqsh.p3d");
	// ...
	GagSetPersist(1);
	// ...
GagEnd();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.GagBegin("gag_sqsh.p3d")
	-- ...
	Game.GagSetPersist(1)
	-- ...
Game.GagEnd()
```
{{ endtab }}
{{ endtabs }}

# Notes
If the gag is set to sparkle via [[GagSetSparkle.md]] but has already been completed, sparkles will be forcefully disabled.