---
title: "Engine.Vector3.ClampMagnitude"
description: "Provides information about the Engine.Vector3.ClampMagnitude function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Clamps the magnitude of a vector to a specified maximum length.

# Syntax
```lua
Engine.Vector3.ClampMagnitude( vector, maxLength )
```

## Arguments
* **vector** (Vector3): The vector to clamp.
* **maxLength** (number): The maximum length of the vector.

## Return Values
* (Vector3): A vector with its magnitude clamped to the specified maximum length.

# Examples
```lua
local vector = Engine.Vector3(1, 2, 3)
local maxLength = 2
local result = Engine.Vector3.ClampMagnitude(vector, maxLength)
```