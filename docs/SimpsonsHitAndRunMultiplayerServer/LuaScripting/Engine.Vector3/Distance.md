---
title: "Engine.Vector3.Distance"
description: "Provides information about the Engine.Vector3.Distance function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Calculates the distance between two vectors.

# Syntax
```lua
Engine.Vector3.Distance( vectorA, vectorB )
```

## Arguments
* **vectorA** (Vector3): The first vector.
* **vectorB** (Vector3): The second vector.

## Return Values
* (number): The distance between the two vectors.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local result = Engine.Vector3.Distance(vectorA, vectorB)
```