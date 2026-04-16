---
title: "SetCondSound"
description: "Set a sound to use for a hitpeds condition or the insidetrigger / outsidetrigger conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a sound to use for the following ASF conditions:

* [[../MissionConditions/hitpeds.md]]
* [[../MissionConditions/insidetrigger-outsidetrigger.md]]

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
## hitpeds Condition
{{ tabs }}
{{ tab MFK }}
```js
SetCondSound( sound );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondSound( sound )
```
{{ endtab }}
{{ endtabs }}

* **sound**: The name of the daSoundResourceData to play.

## insidetrigger / outsidetrigger Conditions
{{ tabs }}
{{ tab MFK }}
```js
SetCondSound( sound, event, [time_between, start_delay] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondSound( sound, event, [time_between, start_delay] )
```
{{ endtab }}
{{ endtabs }}

* **sound**: The name of the daSoundResourceData to play.
* **event**: The event to play the sound on.
    * **enter_trigger**: Play the sound when entering the trigger.
    * **inside_trigger**: Play the sound when inside the trigger 
        * Only for "insidetrigger" conditions.
    * **outside_trigger**: Play the sound when outside the trigger 
        * Only for "outsidetrigger" conditions.
    * **exit_trigger**: Play the sound when exiting the trigger.
* **time_between**: The time between each time the sound plays in second 
    * Only for "inside_trigger" or "outside_trigger" events.
* **start_delay**: The delay before the sound starts playing after entering/exiting the trigger in seconds 
    * Only for "inside_trigger" or "outside_trigger" events.


# Examples
## hitpeds Condition
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	SetCondSound("generic_car_explode");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	Game.SetCondSound("generic_car_explode")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

## insidetrigger / outsidetrigger Conditions
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");

	SetCondSound("enter_trigger","gag_alm2");
	SetCondSound("inside_trigger","countdown_beeps",1,5);
	SetCondSound("exit_trigger","P_HitByC_Mrg_01");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")

	Game.SetCondSound("enter_trigger","gag_alm2")
	Game.SetCondSound("inside_trigger","countdown_beeps",1,5)
	Game.SetCondSound("exit_trigger","P_HitByC_Mrg_01")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}
