---
title: "AddNPC"
description: "Adds an NPC to the world in an objective."
authors: [ 2, 104 ]
---

Adds an NPC to the world in an objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddNPC( npc, locator, [unused] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPC( npc, locator, [unused] )
```
{{ endtab }}
{{ endtabs }}

* **npc**: The name of the NPC to add.
* **locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] to place the NPC on.
* **unused**: Unused.
	* Optional.
	* Seemingly was meant to refer to an interior name, based on Radical's scripts, but does nothing.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("dummy");
	AddNPC("ned", "m2_ned_sd");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("dummy")
	Game.AddNPC("ned", "m2_ned_sd")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}