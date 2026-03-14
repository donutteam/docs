---
title: "Engine.Vector3.Max"
description: "Provides information about the Engine.Vector3.Max function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a vector that is made up of the largest components of two vectors.

# Syntax
```lua
Engine.Vector3.Max( vectorA, vectorB )
```

## Arguments
* **vectorA** (Vector3): The first vector.
* **vectorB** (Vector3): The second vector.

## Return Values
* (Vector3): A vector containing the largest components of the two input vectors.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local result = Engine.Vector3.Max(vectorA, vectorB)
```