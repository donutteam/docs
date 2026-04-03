---
title: "Engine.VectorUtil.InSphere"
description: "Provides information about the Engine.VectorUtil.InSphere function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a point is inside a sphere.

# Syntax
```lua
Engine.VectorUtil.InSphere( point, sphereCenter, sphereRadius )
```

## Arguments
* **point** ([[../Engine.Vector3.md|Vector3]]): The point to check.
* **sphereCenter** ([[../Engine.Vector3.md|Vector3]]): The center of the sphere.
* **sphereRadius** (number): The radius of the sphere.

## Return Values
* (boolean): True if the point is inside the sphere, false otherwise.

# Examples
```lua
local point = Engine.Vector3(1, 2, 3)
local sphereCenter = Engine.Vector3(4, 5, 6)
local sphereRadius = 5
local inSphere = Engine.VectorUtil.InSphere(point, sphereCenter, sphereRadius)
```