---
title: "SetConditionalParameter"
description: "Set parameters on a car depending on various conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

Set parameters on a car depending on various conditions.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
## drawableVisibility Parameter
{{ tabs }}
{{ tab CON }}
```js
SetConditionalParameter("drawableVisibility", vehicle_drawable_name, condition, [condition_value1, ...]);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetConditionalParameter("drawableVisibility", vehicle_drawable_name, condition, [condition_value1, ...])
```
{{ endtab }}
{{ endtabs }}

* **"drawableVisibility"**: This type of parameter sets the visibility of a drawable on the car if the condition is true.
* **vehicle_drawable_name**: The name of the drawable on the vehicle to show/hide.
* **condition**: The condition that determines if the prop is visible.
    * **vehicleHealth**: A condition that depends on the health of the vehicle.
        * This condition requires 2 more arguments specifying the minimum health and the maximum health for the condition to be true.
    * **level**: A condition that depends on the level the player is currently in.
        * This condition requires an argument specifying the level that the condition will return true in.

## hasdoors Parameter
{{ tabs }}
{{ tab CON }}
```js
SetConditionalParameter("hasdoors", condition, [condition_value1, ...]);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetConditionalParameter("hasdoors", condition, [condition_value1, ...])
```
{{ endtab }}
{{ endtabs }}

* **"hasdoors"**: This type of parameter controls whether or not the car has doors if the condition is true.
* **condition**: See the "drawableVisibility" section.

## highroof Parameter
{{ tabs }}
{{ tab CON }}
```js
SetConditionalParameter("highroof", condition, [condition_value1, ...]);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetConditionalParameter("highroof", condition, [condition_value1, ...])
```
{{ endtab }}
{{ endtabs }}

* **"highroof"**: This type of parameter controls whether or not the car has a high roof if the condition is true.
* **condition**: See the "drawableVisibility" section.

# Examples

{{ tabs }}
{{ tab CON }}
```js
SetConditionalParameter("drawableVisibility", "clfamilyRoof", "vehicleHealth", 0.5, 3.0); 
SetConditionalParameter("drawableVisibility", "clfamilyFood", "level", 1); 

SetConditionalParameter("hasDoors", "vehicleHealth", 1.5, 3.0);

SetConditionalParameter("highRoof", "vehicleHealth", 0.0, 0.5);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetConditionalParameter("drawableVisibility", "clfamilyRoof", "vehicleHealth", 0.5, 3.0)
Game.SetConditionalParameter("drawableVisibility", "clfamilyFood", "level", 1)

Game.SetConditionalParameter("hasDoors", "vehicleHealth", 1.5, 3.0)

Game.SetConditionalParameter("highRoof", "vehicleHealth", 0.0, 0.5)
```
{{ endtab }}
{{ endtabs }}