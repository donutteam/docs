---
title: "Engine.VectorUtil.InBox"
description: "Provides information about the Engine.VectorUtil.InBox function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a point is inside a box.

# Syntax
```lua
Engine.VectorUtil.InBox( point, boxMin, boxMax )
```

## Arguments
* **point** ([[../Engine.Vector3.md|Vector3]]): The point to check.
* **boxMin** ([[../Engine.Vector3.md|Vector3]]): The minimum corner of the box.
* **boxMax** ([[../Engine.Vector3.md|Vector3]]): The maximum corner of the box.

## Return Values
* (boolean): True if the point is inside the box, false otherwise.

# Examples
```lua
local point = Engine.Vector3(1, 2, 3)
local boxMin = Engine.Vector3(4, 5, 6)
local boxMax = Engine.Vector3(7, 8, 9)
local inBox = Engine.VectorUtil.InBox(point, boxMin, boxMax)
```