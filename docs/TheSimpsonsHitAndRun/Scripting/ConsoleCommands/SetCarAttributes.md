---
title: "SetCarAttributes"
description: "Sets attributes for a car in the phonebooth."
authors: [ 2 ]
---

Sets attributes for a car in the phonebooth.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/Rewards.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCarAttributes( name, top_speed, acceleration, toughness, handling );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCarAttributes( name, top_speed, acceleration, toughness, handling )
```
{{ endtab }}
{{ endtabs }}

* **name**: The internal name of the car.
* **top_speed**: Sets how many stars this car will have for the top speed attribute.
	* Use `0` to `5`. Half values such as `1.5` are also supported.
* **acceleration**: Sets how many stars this car will have for the acceleration attribute.
	* Use `0` to `5`. Half values such as `1.5` are also supported.
* **toughness**: Sets how many stars this car will have for the toughness attribute.
	* Use `0` to `5`. Half values such as `1.5` are also supported.
* **handling**: Sets how many stars this car will have for the handling attribute.
	* Use `0` to `5`. Half values such as `1.5` are also supported.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Both are valid
SetCarAttributes("famil_v", 1, 1.5, 2.5, 4);
SetCarAttributes("famil_v", 1.0, 1.5, 2.5, 4.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Both are valid
Game.SetCarAttributes("famil_v", 1, 1.5, 2.5, 4)
Game.SetCarAttributes("famil_v", 1.0, 1.5, 2.5, 4.0)
```
{{ endtab }}
{{ endtabs }}

# Notes
By default, you can register attributes for up to 50 cars.

Mods can bypass this limit by requiring the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/IncreasedRewardLimits.md]] hack.