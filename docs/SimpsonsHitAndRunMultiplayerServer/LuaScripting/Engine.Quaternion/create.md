---
title: "Engine.Quaternion.create"
description: "Provides information about the Engine.Quaternion.create function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Creates a quaternion from the specified components (x, y, z, w).

# Syntax
Either of the following syntaxes can be used to create a quaternion:
```lua
Engine.Quaternion.create( x, y, z, w )
Engine.Quaternion( x, y, z, w )
```

## Arguments
* **x** (number): The x component of the quaternion.
* **y** (number): The y component of the quaternion.
* **z** (number): The z component of the quaternion.
* **w** (number): The w component of the quaternion.

## Return Values
* (Quaternion): A quaternion with the specified components.

# Examples
```lua
local quat1 = Engine.Quaternion.create(0, 0, 0, 1) -- Creates an identity quaternion
local quat2 = Engine.Quaternion(0.7071, 0, 0, 0.7071) -- Creates a quaternion representing a rotation of 90 degrees around the X-axis
```