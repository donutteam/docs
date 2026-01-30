---
title: Custom Interior Support
description: "This hack allows mods to modify interior definitions and add custom ones."
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to modify interior definitions and add custom ones.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomInteriorSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomInteriorSupport.ini` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab Mirror Example }}
```ini
; [Interior] Section
	; Name: The name of the interior. Used in Interior Entrance locators.
	; Level: Specify what Level the interior is in. Repeat for each level.
	; ResetAmbientCharacter: Specify an Ambient Character who will have their position reset when you enter the interior. Repeat for each character.
	; ShapeType: The type of shape that represents the area the interior encompasses.
		; Sphere: Use a sphere to define where the interior is.
		; Box: Use a box to define where the interior is.
		
		; Sphere ShapeType
	; X: The X position of the sphere.
	; Y: The Y position of the sphere.
	; Z: The Z position of the sphere.
	; Radius: The radius of the sphere.
	
		; Box ShapeType
	; MinX: The minimum X position in the box.
	; MinY: The minimum Y position in the box.
	; MinZ: The minimum Z position in the box.
	; MaxX: The maximum X position in the box.
	; MaxY: The maximum Y position in the box.
	; MaxZ: The maximum Z position in the box.
	
		; Mirror Matrix
	; MirrorXX
	; MirrorXY
	; MirrorXZ
	; MirrorXW
	; MirrorYX
	; MirrorYY
	; MirrorYZ
	; MirrorYW
	; MirrorZX
	; MirrorZY
	; MirrorZZ
	; MirrorZW
	; MirrorWX
	; MirrorWY
	; MirrorWZ
	; MirrorWW

[Interior]
Name=MotelRoom

ShapeType=Sphere
X=-52
Y=0
Z=986
Radius=15.0

Level=4

MirrorXX=1.0
MirrorXY=0.0
MirrorXZ=0.0
MirrorXW=0.0

MirrorYX=0.0
MirrorYY=1.0
MirrorYZ=0.0
MirrorYW=0.0

MirrorZX=0.0
MirrorZY=0.0
MirrorZZ=-1.0
MirrorZW=0.0

MirrorWX=0.0
MirrorWY=0.0
MirrorWZ=1980.115272	; This has to be 2x what the actual Z position of the mirror object for some reason
MirrorWW=1.0
```
{{ endtab }}
{{ tab Ambient Character Example }}
```ini
[Interior]
Name=LoadingDock

ShapeType=Sphere
X=-252
Y=0
Z=986
Radius=24.0

Level=4

; Reset Agent S. when entering this interior.
ResetAmbientCharacter=agents
```
{{ endtab }}
{{ tab Box Shape Interior Example }}
```ini
[Interior]
Name=ExampleBoxShapeInterior

Level=4

ShapeType=Box
MinX=100
MinY=100
MinZ=100
MaxX=120
MaxY=120
MaxZ=120
```
{{ endtab }}
{{ tab Default Interiors }}
```ini
[Interior]
Name=SpringfieldElementary
ShapeType=Sphere
X=500.0
Y=-20.0
Z=-350.0
Radius=24.0
Level=1
Level=4
Level=7

[Interior]
Name=KwikEMart
ShapeType=Sphere
X=500.0
Y=-20.0
Z=-300.0
Radius=24.0
Level=1
Level=4
Level=7

[Interior]
Name=SimpsonsHouse
ShapeType=Sphere
X=500.0
Y=-20.0
Z=-400.0
Radius=24.0
Level=1
Level=4
Level=7

[Interior]
Name=dmv
ShapeType=Sphere
X=0.0
Y=-20.0
Z=-200.0
Radius=24.0
Level=2
Level=5

[Interior]
Name=moe1
ShapeType=Sphere
X=50.0
Y=-20.0
Z=-200.0
Radius=24.0
Level=2
Level=5
MirrorXX=-1.0
MirrorXY=0.0
MirrorXZ=0.0
MirrorXW=0.0
MirrorYX=0.0
MirrorYY=1.0
MirrorYZ=0.0
MirrorYW=0.0
MirrorZX=0.0
MirrorZY=0.0
MirrorZZ=1.0
MirrorZW=0.0
MirrorWX=109.5
MirrorWY=0.0
MirrorWZ=0.0
MirrorWW=1.0
ResetAmbientCharacter=moe

[Interior]
Name=Android
ShapeType=Sphere
X=0.0
Y=-20.0
Z=-350.0
Radius=24.0
Level=3
Level=6

[Interior]
Name=Observatory
ShapeType=Sphere
X=150.0
Y=-20.0
Z=-350.0
Radius=24.0
Level=3
Level=6

[Interior]
Name=bartroom
ShapeType=Sphere
X=500.0
Y=-20.0
Z=-450.0
Radius=24.0
Level=1
Level=4
Level=7
MirrorXX=1.0
MirrorXY=0.0
MirrorXZ=0.0
MirrorXW=0.0
MirrorYX=0.0
MirrorYY=1.0
MirrorYZ=0.0
MirrorYW=0.0
MirrorZX=0.0
MirrorZY=0.0
MirrorZZ=-1.0
MirrorZW=0.0
MirrorWX=0.0
MirrorWY=0.0
MirrorWZ=-894.0
MirrorWW=1.0
```
{{ endtab }}
{{ endtabs }}

# Version History
## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/CustomInteriorSupport.md }}

## Version 1.18.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.2/Hacks/CustomInteriorSupport.md }}