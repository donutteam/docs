---
title: "Dyna Load Data"
description: "Dyna Load Data refers to a type of string that lists a series of zone P3D files and/or World Sphere chunks to load/unload or enable/disable."
authors: [ 2 ]
---

Dyna Load Data refers to a type of string that lists a series of zone P3D files and/or [[/Pure3DFiles/ChunkTypes/WorldSphere.md]] chunks, each followed by a symbol that instructs the game to load/unload the zone or enable/disable the world sphere respectively.

They can be found in [[/Pure3DFiles/ChunkTypes/Locator.md|Type 5 DynamicZone Locators]] and are also used in various script commands such as [[Scripting/ConsoleCommands/SetDynaLoadData.md]].

# Symbols
This table contains the various symbols used in these strings and what type of purpose they serve.

| Symbol | Purpose              |
|--------|----------------------|
| ;      | Region Load          |
| :      | Region Unload        |
| @      | Interior Load        |
| $      | Interior Unload      |
| *      | Enable World Sphere  |
| &      | Disable World Sphere |

# Examples
```
l1z3.p3d:l1z4.p3d:l1z6.p3d:l1z7.p3d:l1r3.p3d:l1r4a.p3d:l1r4b.p3d:l1r6.p3d:l1r7.p3d:l1z1.p3d;l1r1.p3d;l1z2.p3d;l1r2.p3d;
```
```
visibility_testController&
```
```
l1z7.p3d:l1z2.p3d:l1i02.p3d@
```