---
title: "Engine.Vector3.create"
description: "Provides information about the Engine.Vector3.create function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Creates a vector from the specified components (x, y, z).

# Syntax
Either of the following syntaxes can be used to create a vector:
```lua
Engine.Vector3.create( x, y, z )
Engine.Vector3( x, y, z )
```

## Arguments
* **x** (number): The x component of the vector.
* **y** (number): The y component of the vector.
* **z** (number): The z component of the vector.

## Return Values
* (Vector3): A vector with the specified components.

# Examples
```lua
local vec1 = Engine.Vector3.create(0, 0, 0) -- Creates a zero vector
local vec2 = Engine.Vector3(1, 2, 3) -- Creates a vector with components (1, 2, 3)
```