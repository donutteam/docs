---
title: "AddObjective"
description: "Adds an objective to a stage in a mission."
authors: [ 2 ]
---

Adds an objective to a stage in a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddObjective( objective_type, [ arrow_type ]);
AddObjective( objective_type, [ gamble_string, arrow_type ]);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective( objective_type, [ arrow_type ])
Game.AddObjective( objective_type, [ gamble_string, arrow_type ])
```
{{ endtab }}
{{ endtabs }}

* **objective_type**: The objective type.
* **gamble_string**: The string **gamble**.
	* When the objective is [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/race.md]] and the 2nd argument is **gamble**, the race will be set to be a gamble race.
	* Otherwise, including this string does nothing.
* **arrow_type**: The type of road arrows to use in this stage.
	* **BOTH**/**both**/**b**: Place road arrows on both the nearest road and intersections.
	* **NEITHER**/**neither**/**n**: Do not place road arrows.
	* **INTERSECTION**/**intersection**/**i**: Place road arrows on intersections.
	* **NEAREST ROAD**/**nearest road**: Place road arrows on the nearest road.
		* The game also checks for **n** for this **arrow_type**, but having already checked it for **NEITHER**/**neither**/**n**, this check can never be true.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("getin", "neither");
	// ...
CloseObjective();
```
```js
AddObjective("race", "gamble");
	// ...
CloseObjective();
```
```js
AddObjective("race", "gamble", "neither");
	// ...
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("getin", "neither")
	-- ...
Game.CloseObjective()
```
```lua
Game.AddObjective("race", "gamble")
	-- ...
Game.CloseObjective()
```
```lua
Game.AddObjective("race", "gamble", "neither")
	-- ...
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
The actual code for checking **arrow_type** compares the *last* argument against all valid arrow types, not specifically the second or third (depending on the presence of gamble). This code is stupid, hence the documentation above not acknowledging this weird behaviour.