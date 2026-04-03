---
title: "Engine.VectorUtil.InArea"
description: "Provides information about the Engine.VectorUtil.InArea function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a point is inside an area defined by a set of points.

# Syntax
```lua
Engine.VectorUtil.InArea( point, areaCenter, areaSize )
```

## Arguments
* **point** ([[../Engine.Vector3.md|Vector3]]): The point to check.
* **areaCenter** ([[../Engine.Vector3.md|Vector3]]): The center of the area.
* **areaSize** ([[../Engine.Vector3.md|Vector3]]): The size of the area (width, length, height).

## Return Values
* (boolean): True if the point is inside the area, false otherwise.

# Examples
```lua
local point = Engine.Vector3(1, 2, 3)
local areaCenter = Engine.Vector3(4, 5, 6)
local areaSize = Engine.Vector3(7, 8, 9)
local inArea = Engine.VectorUtil.InArea(point, areaCenter, areaSize)
```