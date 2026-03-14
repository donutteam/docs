---
title: "Engine.Quaternion"
description: "Provides information about the Engine.Quaternion table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `Engine.Quaternion` table provides functions for working with quaternions.

## Variables
| Variable Name                | Description                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------|
| `Engine.Quaternion.identity` | A quaternion representing no rotation (0, 0, 0, 1).                                            |
| `Engine.Quaternion.up`       | A quaternion representing a rotation of 90 degrees around the X-axis (0.7071, 0, 0, 0.7071).   |
| `Engine.Quaternion.down`     | A quaternion representing a rotation of -90 degrees around the X-axis (0.7071, 0, 0, -0.7071). |
| `Engine.Quaternion.left`     | A quaternion representing a rotation of 90 degrees around the Y-axis (0, 0.7071, 0, 0.7071).   |
| `Engine.Quaternion.right`    | A quaternion representing a rotation of -90 degrees around the Y-axis (0, 0.7071, 0, -0.7071). |
| `Engine.Quaternion.forward`  | A quaternion representing a rotation of 90 degrees around the Z-axis (0, 0, 0.7071, 0.7071).   |
| `Engine.Quaternion.backward` | A quaternion representing a rotation of -90 degrees around the Z-axis (0, 0, 0.7071, -0.7071). |

## Methods
| Function Name                   | Description                                                      |
|---------------------------------|------------------------------------------------------------------|
| [[Engine.Quaternion/create.md]] | Creates a quaternion from the specified components (x, y, z, w). |

## Metatable
| Metamethod Name | Description                                |
|-----------------|--------------------------------------------|
| `__call`        | Alias for [[Engine.Quaternion/create.md]]. |