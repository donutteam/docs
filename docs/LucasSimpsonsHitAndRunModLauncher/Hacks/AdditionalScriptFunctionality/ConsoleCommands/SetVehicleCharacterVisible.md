---
title: "SetVehicleCharacterVisible"
description: "Set whether or not the character is visible."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Set whether or not the character added via [[AddVehicleCharacter.md]] is visible.

This can be used to force a character to be visible in a car where the driver and player character are not.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterVisible( character );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterVisible( character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterVisible("apu");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterVisible("apu")
```
{{ endtab }}
{{ endtabs }}