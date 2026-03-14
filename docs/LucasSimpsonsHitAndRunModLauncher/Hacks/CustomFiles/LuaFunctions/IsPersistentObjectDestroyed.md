---
title: "IsPersistentObjectDestroyed"
description: "Checks if the given persistent object in a sector has been destroyed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27 
---

Checks if the given persistent object in a sector has been destroyed.

Persistent objects include various props, such as cola crates and cola machines, as well as coins and wasp cameras.

# Syntax
```lua
IsPersistentObjectDestroyed( sector, persistent_object )
```

## Arguments
* **sector** (integer): The sector to check.
	* For convenience, constants for all valid sectors are provided in the [[../LuaTables/PersistentObjectSector.md]] table.
* **persistent_object** (integer): The persistent object to check.
	* Between 1 and 128 (the max amount of persistent objects in a sector).

## Return Values
* (boolean | nil): If the player has completed the gag or `nil` if unavailable.

# Examples
```lua
-- This is l1_crate_Shape -> l1_crate4 in the base game
local DestroyedThatSpecificColaCrate = IsPersistentObjectDestroyed(PersistentObjectSector.L1Z1, 2)
if DestroyedThatSpecificColaCrate then
	-- Do something if Homer has destroyed that specific cola crate
end
```

# Notes
Persistent object indices depend on the order of the relevant chunks in region P3Ds or, for wasp cameras, the order they are added in the level's initialisation script (via [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/AddSpawnPoint.md]] or [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/AddSpawnPointByLocatorScript.md]])

To see which indice refers to which prop/coin/wasp in the base game, see [[/TheSimpsonsHitAndRun/PersistentObjects.md]].