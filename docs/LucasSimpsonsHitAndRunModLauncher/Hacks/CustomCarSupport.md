---
title: "Custom Car Support"
description: "This hack adds support for registering custom cars and adjusting parameters on existing ones."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 350 # 1.6
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack adds support for registering custom cars and adjusting parameters on existing ones.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomCarSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomCarSupport.ini` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab Car Section }}
```ini
[Car]
; Name
;	The internal name of the car.
;
;	NOTE: The [Car] section and the Name property were added in Version 1.26. 
;		If you're targetting an older version, please see the Deprecated Features tab for how to define custom cars.
Name=custom

; Index
; 	Set the index for this car.
; 	This is used for the car camera data chunks in the car's P3D file.
; 	Custom cars can use indices 97 through 255.
Index=97

; Abductable 
; 	Sets whether or not a car can be abducted by the UFO.
; 	Defaults to 0 for certain base game cars or if Invincible is 1.
Abductable=1

; NoHusk 
; 	Sets whether or the husk spawning when the car explodes will be disabled.
NoHusk=0

; NoSkidMarks
; 	Sets whether or not show all the skid marks.
NoSkidMarks=0

; NoFrontSkidMarks 
; 	Sets whether or not to show the front skid marks.
NoFrontSkidMarks=0

; ShadowVisible 
; 	Sets whether or not to show the shadow.
ShadowVisible=1

; Recolourable 
; 	Sets whether or not to allow the vehicle to be recoloured (only works for Traffic Vehicles).
; 	Defaults to 1 for certain base game traffic vehicles as well as if IsHusk is 1.
Recolourable=0

; PreviewScale 
; 	Set the scale of the car in car shops and the phonebooth (if 3DPhoneBoothPreviewSupport).
; 	Defaults to 1.
PreviewScale=1

; NoBumperCam
; 	Sets whether or not the bumper cam can be used in this car.
; 	Defaults to 1 for dune_v and 0 for every other car.
NoBumperCam=0

; Husk 
; 	Sets the husk for this car.
; 	The target car should have IsHusk set to 1!
; 	Defaults to huskA.
Husk=huskA

; IsHusk
; 	Sets whether or not this car is a husk.
; 	Defaults to 1 for huskA and 0 for every other car.
IsHusk=0

; RearWheelSparks
; 	Sets whether or not sparks emit from the back wheels of this car.
; 	Defaults to 1 if IsHusk is 1.
RearWheelSparks=0

; Invincible
; 	Sets whether or not this car can take damage and be destroyed.
; 	Defaults to 1 if IsHusk is 1.
Invincible=0

; FrontSteeringVisualMultiplier / RearSteeringVisualMultiplier
;	Sets a multiplier for how much the front and rear wheels turn when steering the car respectively.
;	Defaults to 1 for the front wheels and 0 for the rear wheels.
FrontSteeringVisualMultiplier=1
RearSteeringVisualMultiplier=0

; Wheel?SteeringVisualMultiplier
;	Set a multiplier for how much a specific wheel turns when steering the car.
;	Defaults to 1 for wheels 2 and 3 and 0 for wheels 0 and 1.
Wheel0SteeringVisualMultiplier=0
Wheel1SteeringVisualMultiplier=0
Wheel2SteeringVisualMultiplier=1
Wheel3SteeringVisualMultiplier=1

; FakeWheel
;	Adds a fake wheel to this car. 
;	This references a FakeWheel section by name, see the tab above for more details.
;	Repeat to add multiple FakeWheels.
FakeWheel=MyFakeWheel

; FrontSkidMarkWidthMultiplier / RearSkidMarkWidthMultiplier 
;	Sets a multiplier for how large the front and rear wheels skid marks should be, relative to their collision objects.
;	Defaults to 1.
FrontSkidMarkWidthMultiplier=1
RearSkidMarkWidthMultiplier=1

; Wheel?SkidMarkWidthMultiplier
;	Set a multiplier for how large the skid marks of a specific wheel should be, relative to its collision object.
;	Defaults to 1.
Wheel0SkidMarkWidthMultiplier=1
Wheel1SkidMarkWidthMultiplier=1
Wheel2SkidMarkWidthMultiplier=1
Wheel3SkidMarkWidthMultiplier=1

```
{{ endtab }}

{{ tab FakeWheel Section }}
```ini
[FakeWheel]
; Name
;	The name of the wheel, referenced by [Car] sections.
Name=Wheel5

; Joint
;	The joint the wheel rotations and other aspects of the real wheel are applied to.
Joint=w5

; CopyRotation
;	Specify which real wheel(s) to copy the rotation of (0, 1, 2 and/or 3)
;	Repeat to add together the rotation of multiple real wheels.
CopyRotation=0

; CopySuspension
;	Specify which real wheel(s) to copy the suspension of (0, 1, 2 and/or 3)
;	Repeat to copy from multiple real wheels, the highest wheel at any given time will be copied.
CopySuspension=0

; SteeringMultiplier
;	Set a multiplier for how much this wheel turns when you steer the car.
;	Defaults to 0.
SteeringMultiplier=0

; CopySkidMarks
;	Specify which real wheel(s) to copy skid marks from (0, 1, 2 or 3)
;	Repeat to copy the skid marks of multiple real wheels (though why would you want to?)
CopySkidMarks=0

; SkidMarkWidthMultiplier
;	Set a multiplier for how wide this wheel's skidmarks are relative to the wheel it is copying the skid marks of.
;	Defaults to 1.
SkidMarkWidthMultiplier=1

[FakeWheel]
Name=Wheel6
Joint=w6
CopyRotation=1
CopySuspension=1
SteeringMultiplier=0
CopySkidMarks=1
SkidMarkWidthMultiplier=1

[Car]
Name=sixwheel

...

FakeWheel=Wheel5
FakeWheel=Wheel6
```
{{ endtab }}

{{ tab Deprecated Features }}
Prior to Version 1.26, a custom car's internal name would be used as the name of the actual section and there was no `Name` property.
```ini
[custom]
; Properties here
```

Other deprecated features:
```ini
; BackWheelSparks
; 	Sets whether or not sparks emit from the back wheels of this car.
; 	Defaults to 1 if IsHusk is 1.
;
;	Superseded by RearWheelSparks in Version 1.26.
BackWheelSparks=0
```
{{ endtab }}

{{ endtabs }}

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomTrafficSupport.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomTrafficSupport.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomTrafficSupport.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/CustomTrafficSupport.md }}

## Version 1.17
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomTrafficSupport.md }}