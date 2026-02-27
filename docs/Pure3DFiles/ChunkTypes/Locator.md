---
title: "Locator (0x3000005)"
description: "Represents a XYZ position in the world and, depending on the type, various other kinds of data."
authors: [ 2, 6310 ]
---

A Locator chunk represents a XYZ position in the world and, depending on the type, various other kinds of data.

# Data Structure
| Property     | Data Type    | Description |
|--------------|--------------|-------------|
| Name         | string       | TODO        |
| LocatorType  | LocatorTypes | TODO        |
| DataLen      | uint32       | TODO        |
| TypeData     | LocatorData  | TODO        |
| Position     | Vector3      | TODO        |
| TriggerCount | uint32       | TODO        |

# Parents
No valid parents.

# Children
* [[LocatorMatrix.md]]
* [[Spline.md]]
* [[TriggerVolume.md]]

# Types
## Event (Type 0)
Used to trigger various events in the game.

See [[/TheSimpsonsHitAndRun/Events.md]] for more information on available events.

## Script (Type 1)
TODO

## Generic (Type 2)
Used to position wasp cameras, gag models and gag triggers.

This type of locator has no effect unless referenced by a script.

Unlike most trigger volumes, gag triggers are declared in a level's load script and created at runtime instead of being stored as a child of the locator.

## CarStart (Type 3)
Used to position cars, characters and other miscellaneous things in level and mission scripts.

## Spline (Type 4)
TODO

## DynamicZone (Type 5)
Used to execute [[/TheSimpsonsHitAndRun/DynaLoadData.md]].

## Occlusion (Type 6)
TODO

## InteriorEntrance (Type 7)
TODO

## Directional (Type 8)
Used to position the player when they enter an interior.

## Action (Type 9)
Used to create various "action buttons" in the world that the player triggers either by pressing action on them or by entering the trigger. These are used for collectibles such as wrenches and collector cards as well as skin shops. They can also be used to control animated world objects in various ways.

See [[/TheSimpsonsHitAndRun/ActionLocatorTypes.md]].

## FOV (Type 10)
TODO

## BreakableCamera (Type 11)
Unused.

## StaticCamera (Type 12)
TODO

## PedGroup (Type 13)
Changes the active ped group when the player enters one of the locator's child [[TriggerVolume.md|Trigger Volumes]].

## Coin (Type 14)
Used to spawn coins.

Unlike other locator types, when loaded, the locator's position is passed to the game's coin manager and the locator itself is discarded.