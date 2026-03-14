---
title: "Engine.Vector3.Set"
description: "Provides information about the Engine.Vector3.Set function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Sets the components of an existing vector.

# Syntax
Either of the following syntaxes can be used to set the components of a vector:
```lua
Engine.Vector3.Set( vector3, x, y, z )
```

## Arguments
* **vector3** (Vector3): The vector to set the components of.
* **x** (number): The x component of the vector.
* **y** (number): The y component of the vector.
* **z** (number): The z component of the vector.

## Return Values
* (Vector3): A vector with the specified components.

# Examples
```lua
local vector = Engine.Vector3(1, 2, 3)
Engine.Vector3.Set(vector, 4, 5, 6)
```