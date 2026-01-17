---
title: "AddDriver"
description: "Adds an NPC as a driver of a car in an objective."
authors: [ 2 ]
---

Adds an NPC as a driver of a car in an objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddDriver( driver, car );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddDriver( driver, car )
```
{{ endtab }}
{{ endtabs }}

* **driver**: The name of the NPC to add as the driver.
* **car**: The name of the mission car to make the NPC the driver of.
	* This must be a mission car added with [[AddStageVehicle.md]].

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level02/m4i.mfk
AddObjective("race", "both");
	RemoveNPC("snake");
	AddDriver("snake", "snake_v");
	AddCollectible("m4_finish", "finish_line");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level02/m4i.mfk
Game.AddObjective("race", "both")
	Game.RemoveNPC("snake")
	Game.AddDriver("snake", "snake_v")
	Game.AddCollectible("m4_finish", "finish_line")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}