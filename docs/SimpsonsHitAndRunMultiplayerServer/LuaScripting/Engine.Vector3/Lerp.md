---
title: "Engine.Vector3.Lerp"
description: "Provides information about the Engine.Vector3.Lerp function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Linearly interpolates between two vectors.

# Syntax
```lua
Engine.Vector3.Lerp( vectorA, vectorB, t )
```

## Arguments
* **vectorA** (Vector3): The first vector.
* **vectorB** (Vector3): The second vector.
* **t** (number): The interpolation factor (0 to 1).

## Return Values
* (Vector3): The interpolated vector.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local t = 0.5
local result = Engine.Vector3.Lerp(vectorA, vectorB, t)
```