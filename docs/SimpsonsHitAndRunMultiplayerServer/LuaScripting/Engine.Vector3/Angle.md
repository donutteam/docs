---
title: "Engine.Vector3.Angle"
description: "Provides information about the Engine.Vector3.Angle function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Calculates the angle between two vectors.

# Syntax
```lua
Engine.Vector3.Angle( from, to )
```

## Arguments
* **from** (Vector3): The first vector.
* **to** (Vector3): The second vector.

## Return Values
* (number): The angle between the two vectors in radians.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local result = Engine.Vector3.Angle(vectorA, vectorB)
```