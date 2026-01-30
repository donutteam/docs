---
title: "SetVehicleCharacterJumpOut"
description: "Set the character to jump out of the vehicle is destroyed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Set a character added via [[AddVehicleCharacter.md]] to jump out of the vehicle is destroyed.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterJumpOut( character, [direction] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterJumpOut( character, [direction] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **direction**: The direction in which they will jump. This is an angle from 0 to 360 degrees.
    * The default value of this depends on the character's position relative to the origin of the car.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterJumpOut("apu", 180);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterJumpOut("apu", 180)
```
{{ endtab }}
{{ endtabs }}