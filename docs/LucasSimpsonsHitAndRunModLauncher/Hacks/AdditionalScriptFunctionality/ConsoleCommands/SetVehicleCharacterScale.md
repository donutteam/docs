---
title: "SetVehicleCharacterScale"
description: "Set the scale of the character."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Set the scale of the character added via [[AddVehicleCharacter.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterScale( character, [scale] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterScale( character, [scale] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **scale**: The scale of the character.
    * The default value is the scale defined in the CON file for said car.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterScale("apu", 2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterScale("apu", 2)
```
{{ endtab }}
{{ endtabs }}