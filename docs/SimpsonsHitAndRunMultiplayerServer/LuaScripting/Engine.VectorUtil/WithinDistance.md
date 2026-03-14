---
title: "Engine.VectorUtil.WithinDistance"
description: "Provides information about the Engine.VectorUtil.WithinDistance function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if the distance between two points in 2D space is within a specified distance.

# Syntax
```lua
Engine.VectorUtil.WithinDistance( pointA, pointB, distance )
```

## Arguments
* **pointA** (Vector3): The first point.
* **pointB** (Vector3): The second point.
* **distance** (number): The distance to check against.

## Return Values
* (boolean): True if the distance between the two points is less than or equal to the specified distance, false otherwise.

# Examples
```lua
local pointA = Engine.Vector3(1, 2, 3)
local pointB = Engine.Vector3(4, 5, 6)
local distance = 5
local withinDistance = Engine.VectorUtil.WithinDistance(pointA, pointB, distance)
```