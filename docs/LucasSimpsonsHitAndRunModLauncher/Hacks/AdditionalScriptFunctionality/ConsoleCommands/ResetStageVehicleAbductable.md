---
title: "ResetStageVehicleAbductable"
description: "Resets the abductable status of a vehicle set with SetStageVehicleAbductable back to the default for the given vehicle."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This command resets the abductable status of a vehicle set with [[SetStageVehicleAbductable.md]] back to the default for the given vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ResetStageVehicleAbductable( vehicle );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageVehicleAbductable( vehicle )
```
{{ endtab }}
{{ endtabs }}

* **vehicle**: The vehicle you would like to reset the abductable flag on.
	* When using `current`, it will reset the flag for the vehicle that was the player's current vehicle when [[SetStageVehicleAbductable.md]] was called.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
ResetStageVehicleAbductable("skinn_v");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageVehicleAbductable("skinn_v")
```
{{ endtab }}
{{ endtabs }}