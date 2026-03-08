---
title: "Engine.Vector3.Normalize"
description: "Provides information about the Engine.Vector3.Normalize function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a vector with the same direction as the input vector but with a magnitude of 1.

# Syntax
```lua
Engine.Vector3.Normalize( vector )
```

## Arguments
* **vector** (Vector3): The vector to normalize.

## Return Values
* (Vector3): A vector with the same direction as the input vector but with a magnitude of 1.

# Examples
```lua
local vector = Engine.Vector3(1, 2, 3)
local result = Engine.Vector3.Normalize(vector)
```