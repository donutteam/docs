---
title: "AddVehicleCharacter"
description: "This can be used to add additional characters to a car on top of the driver and the player character's."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

This can be used to add additional characters to a car on top of the driver and the player character's.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter( character, [joint, rotation] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter( character, [joint, rotation] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character to add.
* **joint**: The name of the joint to place the character on. Defaults to "pl".
* **rotation**: The rotation of the character on the joint. Defaults to 180.
    * 180 is facing forwards in the car since characters are backwards in this game.

# Examples
{{ tabs }}
{{ tab CON }}
```js
// Add Marge to the Passenger Seat
AddVehicleCharacter("marge");
​
// Add Bart to the Smoke Joint 
//  (you'd probably want to add custom joints to the car for other passengers)
AddVehicleCharacter("bart", "sl", 0);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Add Marge to the Passenger Seat
Game.AddVehicleCharacter("marge")
​
-- Add Bart to the Smoke Joint 
--  (you'd probably want to add custom joints to the car for other passengers)
Game.AddVehicleCharacter("bart", "sl", 0)
```
{{ endtab }}
{{ endtabs }}

# Notes
Characters added using this command cannot be removed from the car via a mission script.