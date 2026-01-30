---
title: "Bug Fixes"
description: "This hack contains a variety of bug fixes for issues in the original game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 368 # 1.15
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack contains a variety of bug fixes for issues in the original game.

**NOTE:** When this hack is required by a mod, the mods settings for it are prioritised over the ones in the hack's settings.

# Settings
## Visual
### Cursor Position
Fixes an issue where the cursor is positioned incorrectly when using an aspect ratio other than 1:1.

### Steering Animations
Fixes an issue preventing steering/swaying animations from playing.

### Character Rotations
Fixes issues where character rotations are handled incorrectly when standing on top of movable objects such as platforms or cars.

### HUD Coin Depth
Makes the coin on the HUD have depth.

### Stuck Brake and Reverse Lights
Fixes some issues where the brake and reverse lights could get stuck on cars.

## Crashes
### Main Menu Cheat Code Enter Crash
Fixes a crash when entering a cheat code on the main menu.

### Unlock All Camera Settings Crash
Fixes a crash related to the Unlock All Cameras cheat and the Settings menu.

### Late Focus Freeze
Fixes the game freezing on the license screen if it's not focused soon enough.

### Zone Load on Exit
**This setting is only available when using the `-testing` [[../CommandLineArguments.md|command line argument]].**
	
Fixes the game crashing if it tries loading a zone on exit.

### Car Deleted While Loading CON File
**This setting is only available when using the `-testing` [[../CommandLineArguments.md|command line argument]].**

Fixes the game crashing if a car is deleted while its CON file is still loading.

### High Coin Count
**This setting is only available when using the `-testing` [[../CommandLineArguments.md|command line argument]].**

Fixes the game crashing if you collect more than 9,999,999 coins.

## Actors
### Restore Wasp Collision
Fixes an issue where Wasp Collision becomes disabled entirely (until the level is reloaded) after destroying some amount of wasp cameras resulting in cars being unable to destroy them.

## Vehicles
### No Air Vent Audio
Fixes an issue where air vent audio still plays when driving into a vent when inside a car.

### Baby Van Tilt
Fixes a famous bug that most notably causes the baby van in Level 5 Mission 3 to be tilted and have incorrect physics. 

This bug as well as this fix both apply to other cars as well though it appears most prominently on this one so it's named after it.

### Phone Booth Camera Pan Active Camera Change
This fixes a bug related to pressing the in-car change camera button during the phonebooth's camera pan. Without this bug fix, doing so will cancel the camera and switch your camera to the mouse controlled camera until the game changes your camera again (such as when getting in a car). If you use mission select to select a mission without getting in a car, you will be able to skip the next mission start camera.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=BugFixes
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `BugFixes.ini` and add the parameters necessary for your mod inside it.

```ini	
[Visual]
; HUDCoinDepth
; 	Set whether or not the coin on the HUD will have depth.
HUDCoinDepth=1

; FixCursorPosition
;   Fixes an issue where the cursor is positioned incorrectly when using an aspect ratio other than 1:1.
FixCursorPosition=1

; FixSteeringAnimations
;   Fixes an issue preventing steering/swaying animations from playing.
FixSteeringAnimations=1

; FixCharacterRotations
;   Fixes an issue where character shadows and radar icons are rotated incorrectly when standing on top of movable objects such as platforms or cars.
FixCharacterRotations=1

; FixStuckBrakeAndReverseLights
;   Fixes some issues where the brake and reverse lights could get stuck on cars.
FixStuckBrakeAndReverseLights=1

[Actors]
; RestoreWaspCollision: 
; 	Set whether or not wasp collision gets re-enabled when spawning a wasp camera.
RestoreWaspCollision=1

[Crashes]
; FixCarDeletedWhileLoadingCONFileCrash
; 	Set whether or not the game will crash if a car is deleted before it's CON file is finished loading.
FixCarDeletedWhileLoadingCONFileCrash=0

; FixZoneLoadOnExitCrash
; 	Set whether or not the game will crash if the game tries to load a zone while exiting.
FixZoneLoadOnExitCrash=0

; RoadArrowPathItemLimitIncludeIntersectionCount
; 	This fixes an issue where intersections are not accounted for when creating an array used by the game to place road arrows when navigating. 
; 	This issue has been particularly apparent in custom maps where certain road network configurations may cause this issue to arise.
RoadArrowPathItemLimitIncludeIntersectionCount=0

; FixHighCoinCountCrash
;	Set whether or not the game will crash if the player collects more than 9,999,999 coins.
FixHighCoinCountCrash=1

; FixMainMenuCheatCodeEnterCrash
;   Fixes a crash when entering cheat codes on the main menu.
FixMainMenuCheatCodeEnterCrash=1

; FixUnlockAllCamerasSettingsCrash
;   Fixes a crash related to the Unlock All Cameras cheat and the Settings menu.
FixUnlockAllCamerasSettingsCrash=1

; FixLateFocusFreeze
;    Fixes the game freezing on the license screen if it's not focused soon enough.
FixLateFocusFreeze=1

[Vehicles]
; NoAirVentAudio
; 	Set whether or not the game will play dialog and an air vent sound when driving into the trigger for an airvent.
NoAirVentAudio=1

[Physics]
; FixUninitialisedArticulatedPhysicsObjectCloneRelativeCentreOfMassAndInertiaMatrixUpdateInterval
; 	Set whether or not a famous bug that most notably causes the baby van in Level 5 Mission 3 to be tilted and have incorrect physics will be fixed.
; 	This bug as well as this fix both apply to other cars as well though it appears most prominently on that one.
FixUninitialisedArticulatedPhysicsObjectCloneRelativeCentreOfMassAndInertiaMatrixUpdateInterval=1

[Camera]
; FixRelativeAnimatedCamCameraChange
; 	Fixes a bug related to pressing the in-car change camera button during the phonebooth's camera pan. 
; 	Without this bug fix, doing so will cancel the camera and switch your camera to the mouse controlled camera until the game changes your camera again (such as when getting in a car). 
; 	If you use mission select to select a mission without getting in a car, you will be able to skip the next mission start camera.
FixRelativeAnimatedCamCameraChange=1
```

# Notes
* All of this hack's settings, except those only shown when using the `-testing` command line argument, are enabled by default.
* Any bug fixes forced on or off with a configuration file will override any user settings for this hack if they have it enabled.

# Version History
## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/BugFixes.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/BugFixes.md }}

## Version 1.23.6
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.6/Hacks/BugFixes.md }}

## Version 1.23.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/BugFixes.md }}

## Version 1.23.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.3/Hacks/BugFixes.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/BugFixes.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/BugFixes.md }}

## Version 1.19
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/BugFixes.md }}

## Version 1.18.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.2/Hacks/BugFixes.md }}

## Version 1.17
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/BugFixes.md }}