---
title: "Engine.VectorUtil.InCircle"
description: "Provides information about the Engine.VectorUtil.InCircle function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a point is inside a circle.

# Syntax
```lua
Engine.VectorUtil.InCircle( point, circleCenter, circleRadius )
```

## Arguments
* **point** (Vector3): The point to check.
* **circleCenter** (Vector3): The center of the circle.
* **circleRadius** (number): The radius of the circle.

## Return Values
* (boolean): True if the point is inside the circle, false otherwise.

# Examples
```lua
local point = Engine.Vector3(1, 2, 3)
local circleCenter = Engine.Vector3(4, 5, 6)
local circleRadius = 5
local inCircle = Engine.VectorUtil.InCircle(point, circleCenter, circleRadius)
```