---
title: "Engine.Vector3.LerpUnclamped"
description: "Provides information about the Engine.Vector3.LerpUnclamped function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Linearly interpolates between two vectors without clamping the interpolation factor.

# Syntax
```lua
Engine.Vector3.LerpUnclamped( vectorA, vectorB, t )
```

## Arguments
* **vectorA** (Vector3): The first vector.
* **vectorB** (Vector3): The second vector.
* **t** (number): The interpolation factor.

## Return Values
* (Vector3): The interpolated vector.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local t = 0.5
local result = Engine.Vector3.LerpUnclamped(vectorA, vectorB, t)
```