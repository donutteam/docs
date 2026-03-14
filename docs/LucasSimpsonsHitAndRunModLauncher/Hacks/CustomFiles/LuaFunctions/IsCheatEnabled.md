---
title: "IsCheatEnabled"
description: "Checks if the given cheat flags are enabled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if the given cheat flags are enabled.

# Syntax
```lua
IsCheatEnabled( cheat_flags )
```

## Arguments
* **cheat_flags** (integer): The cheat(s) to check.
	* For convenience, constants for all valid cheats are provided in the [[../LuaTables/Cheat.md]] table.

## Return Values
* (boolean): If the cheat(s) are enabled.

# Examples
```lua
-- Check if the player has an invincible car
local InvincibleCarCheatEnabled = IsCheatEnabled(Cheat.InvincibleCar)

-- You can also use the Bitwise OR operator to check if multiple cheats are enabled concurrently
--	All of them must be enabled for this to return true
local AllCheatsEnabled = IsCheatEnabled(Cheat.HighAcceleration | Cheat.InvincibleCar)
```