---
title: "Engine.Vector3.Add"
description: "Provides information about the Engine.Vector3.Add function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Adds two vectors together and returns the result.

# Syntax
```lua
Engine.Vector3.Add( vectorA, vectorB )
```

## Arguments
* **vectorA** (Vector3): The first vector to add.
* **vectorB** (Vector3): The second vector to add.

## Return Values
* (Vector3): A vector with the specified components.

# Examples
```lua
local vectorA = Engine.Vector3(1, 2, 3)
local vectorB = Engine.Vector3(4, 5, 6)
local result = Engine.Vector3.Add(vectorA, vectorB)
```