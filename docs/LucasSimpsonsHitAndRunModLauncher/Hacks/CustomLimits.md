---
title: "Custom Limits"
description: "This allows mods to customise various limits in the game to suit their needs."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 367 # 1.14
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This allows mods to customise various limits in the game to suit their needs.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomLimits
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomLimits.ini` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab Current Features }}
```ini
[Miscellaneous]
; DeletedEntityLimit
; 	Change the number of entities that can be deleted at one time. 
; 	Defaults to 5000.
DeletedEntityLimit=5000

; ActionButtonLimit
; 	Change the maximum number of action buttons. 
; 	Defaults to 128. Must be divisible by 8.
ActionButtonLimit=128

[Roads]
; CubeShapeLimit
; 	The maximum number of Cube Shapes that can exist. 
; 	Defaults to 1200.
CubeShapeLimit=1200

; RoadLimit
; 	The maximum number of Roads that can exist. 
; 	Defaults to 150.
RoadLimit=150

; IntersectionLimit
; 	The maximum number of Intersections that can exist. 
; 	Defaults to 60.
IntersectionLimit=60

; RoadSegmentLimit
; 	The maximum number of Road Segments that can exist. 
; 	Defaults to 1200.
RoadSegmentLimit=1200

[Regions]
; Limit
; 	The maximum number of Regions that can be loaded at once.
; 	This includes the Terra file.
; 	Defaults to 7.

Limit=7
; EntityLimit
; 	The maximum number of entities any one zone can contain. 
; 	Defaults to 2000.
EntityLimit=2000

; RoadSegmentLimit
; 	The maximum number of Road Segments any one zone can contain. 
; 	Defaults to 1250.
; 	Given that Road Segments should only ever be in the Terra file, this should just match the other RoadSegmentLimit in the [Roads] section.
RoadSegmentLimit=1250

[TreeNodes]
; DrawDistance
; 	The maximum distance any part of an object can be from the camera before it stops rendering. 
; 	Defaults to 200.
DrawDistance=200

; BoundsMinimumY
; 	The minimum position on the Y axis in any tree node. 
; 	Defaults to -200. 
; 	Leave blank to use the value in the k-d Tree.
BoundsMinimumY=-200

; BoundsMaximumY
; 	The maximum position on the Y axis in any tree node. 
; 	Defaults to 100. 
; 	Leave blank to use the value in the k-d Tree.
BoundsMaximumY=100

[Billboards]
; QuadGroupLimit
; 	The maximum number of billboard quad groups that can exist. 
; 	Defaults to 25.
QuadGroupLimit=25

; QuadLimit
; 	The maximum number of billboard quads that can exist. 
; 	Defaults to 100.
QuadLimit=100

[CollisionIndices]
; VehicleLimit
; 	The maximum number of vehicle collision indices. 
; 	Defaults to 15.
VehicleLimit=15

; CharacterLimit
; 	The maximum number of character collision indices. 
; 	Defaults to 18.
CharacterLimit=18

; StaticPhysLimit
; 	The maximum number of static phys collision indices. 
; 	Defaults to 30.
StaticPhysLimit=30

; AnimCollLimit
; 	The maximum number of anim coll collision indices. 
; 	Defaults to 20.
AnimCollLimit=20

; FenceLimit
; 	The maximum number of fence collision indices. 
; 	Defaults to 8.
FenceLimit=8

; DynaPhysLimit
; 	The maximum number of dyna phys collision indices. 
; 	Defaults to 20.
DynaPhysLimit=20

[Sound]
; PlayingClipPlayerLimit
; 	The maximum number of simultaneously playing clip players. 
; 	Defaults to 25.
PlayingClipPlayerLimit=25

; PlayingStreamPlayerLimit
; 	The maximum number of simultaneously playing stream players.
; 	Defaults to 8.
PlayingStreamPlayerLimit=8

[Scripting]
; ArgumentLengthLimit
; 	The maximum number of characters in a single argument to a script command.
; 	Defaults to 64 with a maximum of 127. 
; 	The effective limit is one less than what you set (63 by default with a maximum of 126).
ArgumentLengthLimit=64

[AnimEntities]
; DArrowAnimLimit
; 	Defaults to 6.
DArrowAnimLimit=6

; WArrowAnimLimit
; 	Defaults to 6.
WArrowAnimLimit=6

; AnimLimit
; 	Defaults to 100 with a maximum of 127.
AnimLimit=100

; AnimCollLimit
; 	Defaults to 100.
AnimCollLimit=100

; MultiControllerLimit
; 	Defaults to 50.
MultiControllerLimit=50

; StatePropLimit
; 	Defaults to 350.
StatePropLimit=350

[Heaps]
; TempSize
; 	Defaults to 1.0.
TempSize=1.0

; LevelHUDNormalGameSize
; 	Defaults to 2.5.
LevelHUDNormalGameSize=2.5

; LevelHUDBonusGameSize
; 	Defaults to 1.55.
LevelHUDBonusGameSize=1.55

[Cars]
; CarLimit
; 	Change the maximum number of cars that can exist at once.
; 	Defaults to 30 with a maximum of 127.
CarLimit=30

; HuskLimit
; 	Change the maximum number of husks that can exist at once.
; 	Defaults to 5.
HuskLimit=5

; SkidMarkLimit
; 	Change the maximum number of skid marks that can exist at once.
; 	Defaults to 30.
SkidMarkLimit=30

[Missions]
; StageLimit
; 	Change the maximum number of stages in a mission.
;	Defaults to 25.
StageLimit=25

[Pedestrians]
; GroupLimit
; 	Change the maximum number of ped groups that can be defined in a level.
; 	Defaults to 10.
GroupLimit=10

; PathLimit
; 	Change the maximum number of pedstrian paths that can exist. 
; 	Defaults to 125.
PathLimit=125

[Triggers]
; VolumeLimit
; 	Change the maximum number of trigger volumes that can exist at once.
; 	Defaults to 500.
VolumeLimit=500
```
{{ endtab }}
{{ tab Deprecated Features }}
These properties have been superseded by new properties in other sections. They are still supported for backwards compatibility but we don't recommend mods targetting newer versions use these.

```ini
[Miscellaneous]
; CarLimit
; 	Change the maximum number of cars. 
; 	Defaults to 30 with a maximum of 127.
;	
; 	Superseded by CarLimit in the [Cars] section as of 1.24.
CarLimit=30

; PathLimit
; 	Change the maximum number of pedstrian paths that can exist. 
; 	Defaults to 125.
;	
; 	Superseded by PathLimit in the [Pedestrians] section as of 1.25.
PathLimit=125
```
{{ endtab }}
{{ endtabs }}

# Version History
## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomLimits.md }}

## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomLimits.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomLimits.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomLimits.md }}

## Version 1.23.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/CustomLimits.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomLimits.md }}

## Version 1.17.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.2/Hacks/CustomLimits.md }}

## Version 1.16.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16.1/Hacks/CustomLimits.md }}

## Version 1.16
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16/Hacks/CustomLimits.md }}

## Version 1.15.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15.3/Hacks/CustomLimits.md }}

## Version 1.15
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15/Hacks/CustomLimits.md }}