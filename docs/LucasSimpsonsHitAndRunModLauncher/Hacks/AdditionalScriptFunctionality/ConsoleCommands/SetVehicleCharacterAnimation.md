---
title: "SetVehicleCharacterAnimation"
description: "Set the animation that the character will use in the car."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Set the animation that a character added via [[AddVehicleCharacter.md]] will use in the car.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterAnimation( character, animation, [bobbing] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterAnimation( character, animation, [bobbing] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **animation**: The name of the animation.
    * This animation must be specified in the NPD animation set.
* **bobbing**: Whether or not the character will bob up and down.
    * This defaults to false if this function is called.
    * This will also make the character lean side-to-side when appropriate.
    * Though this is dependent on the user's Bug Fixes setting for this.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterAnimation("apu","surf_cycle");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterAnimation("apu","surf_cycle")
```
{{ endtab }}
{{ endtabs }}