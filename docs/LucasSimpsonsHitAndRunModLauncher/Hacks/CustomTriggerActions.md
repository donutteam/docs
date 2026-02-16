---
title: Custom Trigger Actions
description: "This hack allows you to bind custom actions to the triggers of specific locators or events."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 384 # 1.20
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows you to bind custom actions to the triggers of specific locators or events.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomTriggerActions
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomTriggerActions.ini` and add the parameters necessary for your mod inside it.

```ini
; [Action] Section
	; Name: The name of the action (referenced by a CustomTriggerAction).
	; Type: The type of action to use.
		; ChangeTexture: Change a texture of a specific shader.
		; ChangeHUDMapDrawable: Change the current HUD Map Drawable.
		; DestroyCar: Destroy the car that entered the trigger.
		; SetHitAndRunMeter: Set the current value of the Hit & Run Meter.
		; ChangeTrafficGroup: Set the current traffic group. Your mod must use CustomTrafficSupport and enable DynamicGroups for this to do anything.
		; TriggerMusicEvent: Trigger a music event.
		; TiltCamera: Tilt the camera.
		
		; ChangeTexture Type
	; Shader: The name of the shader whose texture you want to change.
	; Texture: The new texture name to set the shader to.
	
		; ChangeHUDMapDrawable Type
	; DrawableName: The name of the drawable to use for the HUD Map.
	
		; DestroyCar Type
	; No extra parameters.

		; SetHitAndRunMeter Type
	; Value: The value to set the meter to. 0 to 100.
	
		; ChangeTrafficGroup Type
	; Value: The traffic group index to use.
	
		; TriggerMusicEvent
	; Event: The name of the event in the current music RMS to trigger. Does nothing if the event does not exist.

		; TiltCamera
	; Value: The angle to tilt the camera to.
	; Duration: How long it takes for the camera to return to normal when leaving the trigger(s).
	; Reset: Whether to reset the camera when changing missions.
	
; [Condition] Section
	; Name: The name of the condition (referenced by a CustomTriggerAction).
	; Type: The type of the condition.
		; Car: The condition will be true if any car enters the trigger.
		; PlayerCar: The condition will be true if the player's car enters the trigger.
		; Character: The condition will be true if any character enters the trigger.
		; Conditions: The condition will be true if all the specified conditions are met.
		; Condition: The condition will be true if any of the specified conditions are met.
		; IsPlayer: The condition will be true if the thing that entered the trigger is the player.
		; Mission: The condition will be true if the player is currently in this mission.
		; UnlockedMission: The condition will be true if the player has this mission unlocked.
		; CompletedMission: The condition will be true if the player has this mission completed.
		; Setting: The condition will be true if the specified mod setting has the specified value.
	; Not: Set if this will be true when the condition is NOT met instead of when it is. Defaults to 0.
	
		; Car/PlayerCar Types
	; CarName: Specify the name of a specific car that will validate the condition.
	; CarIndex: Specify the index of a specific car that will validate the condition.
	
		; Character Type
	; CharacterName: Specify a specific character that will validate the condition.
	
		; Conditions/Condition Types
	; Condition: Specify a sub-condition that will validate the main condition. Repeat for multiple conditions.
        
		; Mission Type
	; Level: The level of the mission that's required to meet the condition. 1-7. Required.
	; Mission: The index of the mission that's required to meet the condition. 0-7 in Level 1, 1-7 in all other levels. Optional.
	; SundayDrive: Specify if the condition should apply to the Sunday Drive mission instead of the main mission. Optional.
	;	OR
	; BonusMission: The index of the bonus mission that's required to meet the condition. 1-5. Optional.
		; The street races are 1-3, the wager race is 4 and the actual bonus mission is 5.
        
		; UnlockedMission Type
	; Level: The level of the mission that's required to meet the condition. 1-7. Required.
	; Mission: The index of the mission that's required to meet the condition. 0-7 in Level 1, 1-7 in all other levels. Required.

		; CompletedMission Type
	; Level: The level of the mission that's required to meet the condition. 1-7. Required.
	; Mission: The index of a story mission that's required to meet the condition. 0-7 in Level 1, 1-7 in all other levels.
	;	OR
	; BonusMission: The index of a bonus mission that's required to meet the condition. 1-5. Required.
		; The street races are 1-3, the wager race is 4 and the actual bonus mission is 5.
		;	Note that 4 will only work if the Wager Race is actually a Wager Race and not something else (like the Taxi Mission in Donut Mod 4)
	; BestTime: Set the best time required in seconds.
		; The game only saves a best time for street races (bonus mission 1-3) if they have a timer.
		; The game only saves a best time for wager races if they're actually a wager race.

		; Setting Type
	; SettingName: The name of the Setting to check.
	; SettingValue: The value the setting must have for the condition to be true.
		; For TickBox settings, valid values are "true", "false", "1" or "0"
	; ModName: The mod name the Setting is in.
		; Optional, defaults to the mod the Condition is declared in.

; [Trigger] Section
	; Name: The name of the trigger (referenced by a CustomTriggerAction).
	; LocatorType: The type of locator whose triggers will be used.
		; 0: If 0 is used, you can specify a specific event index.
		; 9: If 9 is used, you can specify a specific sub-type.
	; LocatorType0Event: Require a specific event index if Type 0 locators are required.
	; LocatorType9Type: Require a specific sub-type if Type 9 locators are required.
	; LocatorName: Match a specific locator name. Repeat for multiple locators.
	; TriggerName: Match a specific trigger name. Repeat for multiple triggers.
	; Condition: Require a specific condition to be met for this trigger to be met. Repeat for multiple conditions. Only one of the specified conditions needs to be met.
	
; [CustomTriggerAction] Section
	; Action: The name of an Action to perform. Repeat for multiple Actions.
	; Condition: Specify a condition that will trigger this when it's met. Repeat for multiple Conditions.
	; PreventDefault: Prevent the default action of the specified Trigger or Event when this CustomTriggerAction occurs.
		; This can cause issues depending on what exactly you're preventing.

	; Event: The index of an event that will trigger this CustomTriggerAction when it occurs. Repeat for multiple Events.
	; Trigger: The name of a trigger required to trigger the action. Repeat for multiple Triggers.

[Action]
Name=TriggerHitAndRun
Type=SetHitAndRunMeter
Value=100

[Condition]
Name=IsL1M1
Type=Mission
Level=1
Mission=1

[Condition]
Name=IsL1M1Sunday
Type=Mission
Level=1
Mission=1
SundayDrive=1

[Condition]
Name=IsL1M2Unlocked
Type=UnlockedMission
Level=1
Mission=2

[Trigger]
Name=glastrucEntry
LocatorType=0
LocatorType0Event=79
LocatorName=glastruc

[Trigger]
Name=WaspTriggers
LocatorType=15

[Trigger]
Name=Z1Phone1
LocatorType=9
LocatorType9Type=SummonVehiclePhone
LocatorName=Z1p1

[CustomTriggerAction]
Action=TriggerHitAndRun
Trigger=glastrucEntry
Condition=IsL1M1Sunday

[CustomTriggerAction]
Action=TriggerHitAndRun
Trigger=Z1Phone1
Condition=IsL1M1

[CustomTriggerAction]
Action=TriggerHitAndRun
Trigger=WaspTriggers
Condition=IsL1M2Unlocked
```

# Debug Text Mode
This hack registers a debug mode for the [[DebugText.md]] hack when used alongside it.

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/1.27/Hacks/CustomTriggerActions.ini }}

## Version 1.23.6
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/1.23.6/Hacks/CustomTriggerActions.ini }}

## Version 1.22.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/1.22.2/Hacks/CustomTriggerActions.ini }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/1.22/Hacks/CustomTriggerActions.ini }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/1.21/Hacks/CustomTriggerActions.ini }}