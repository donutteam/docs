---
title: "Engine.VectorUtil.GetDistance2D"
description: "Provides information about the Engine.VectorUtil.GetDistance2D function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Calculates the distance between two points in 2D space.

# Syntax
```lua
Engine.VectorUtil.GetDistance2D( pointA, pointB )
```

## Arguments
* **pointA** ([[../Engine.Vector3.md|Vector3]]): The first point.
* **pointB** ([[../Engine.Vector3.md|Vector3]]): The second point.

## Return Values
* (number): The distance between the two points.

# Examples
```lua
local pointA = Engine.Vector3(1, 2, 3)
local pointB = Engine.Vector3(4, 5, 6)
local distance = Engine.VectorUtil.GetDistance2D(pointA, pointB)
```