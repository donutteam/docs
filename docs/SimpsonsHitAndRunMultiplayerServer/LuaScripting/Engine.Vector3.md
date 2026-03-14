---
title: "Engine.Vector3"
description: "Provides information about the Engine.Vector3 table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Engine.Vector3` table provides functions for working with 3D vectors.

## Variables
| Variable Name             | Description                                              |
|---------------------------|----------------------------------------------------------|
| `Engine.Vector3.zero`     | A vector with all components equal to 0 (0, 0, 0).       |
| `Engine.Vector3.one`      | A vector with all components equal to 1 (1, 1, 1).       |
| `Engine.Vector3.up`       | A vector representing the up direction (0, 1, 0).        |
| `Engine.Vector3.down`     | A vector representing the down direction (0, -1, 0).     |
| `Engine.Vector3.left`     | A vector representing the left direction (-1, 0, 0).     |
| `Engine.Vector3.right`    | A vector representing the right direction (1, 0, 0).     |
| `Engine.Vector3.forward`  | A vector representing the forward direction (0, 0, 1).   |
| `Engine.Vector3.backward` | A vector representing the backward direction (0, 0, -1). |

## Methods
| Function Name                        | Description                                                                         |
|--------------------------------------|-------------------------------------------------------------------------------------|
| [[Engine.Vector3/create.md]]         | Creates a vector from the specified components (x, y, z).                           |
| [[Engine.Vector3/Set.md]]            | Sets the components of an existing vector.                                          |
| [[Engine.Vector3/Add.md]]            | Adds two vectors together and returns the result.                                   |
| [[Engine.Vector3/Distance.md]]       | Calculates the distance between two vectors.                                        |
| [[Engine.Vector3/Angle.md]]          | Calculates the angle between two vectors in degrees.                                |
| [[Engine.Vector3/ClampMagnitude.md]] | Clamps the magnitude of a vector to a specified maximum.                            |
| [[Engine.Vector3/Cross.md]]          | Calculates the cross product of two vectors.                                        |
| [[Engine.Vector3/Dot.md]]            | Calculates the dot product of two vectors.                                          |
| [[Engine.Vector3/Lerp.md]]           | Linearly interpolates between two vectors by a specified amount.                    |
| [[Engine.Vector3/LerpUnclamped.md]]  | Linearly interpolates between two vectors by a specified amount without clamping.   |
| [[Engine.Vector3/Max.md]]            | Returns a vector that is made from the largest components of two vectors.           |
| [[Engine.Vector3/Min.md]]            | Returns a vector that is made from the smallest components of two vectors.          |
| [[Engine.Vector3/Normalize.md]]      | Returns a vector with the same direction as the original but with a magnitude of 1. |


## Metatable
| Metamethod Name | Description                             |
|-----------------|-----------------------------------------|
| `__call`        | Alias for [[Engine.Vector3/create.md]]. |