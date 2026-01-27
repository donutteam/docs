---
title: "AddObjectiveNPCWaypoint"
description: "Adds a waypoint to an objective NPC."
authors: [ 2 ]
---

Adds an NPC to the world in an objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddObjectiveNPCWaypoint( npc, locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjectiveNPCWaypoint( npc, locator )
```
{{ endtab }}
{{ endtabs }}

* **npc**: The name of the NPC to add a waypoint to.
* **locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] to make them walk to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("dummy");
	AddNPC("ned", "m2_ned_sd");
	AddObjectiveNPCWaypoint("ned", "m2_ned_sd_walk1");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("dummy")
	Game.AddNPC("ned", "m2_ned_sd")
	Game.AddObjectiveNPCWaypoint("ned", "m2_ned_sd_walk1")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}