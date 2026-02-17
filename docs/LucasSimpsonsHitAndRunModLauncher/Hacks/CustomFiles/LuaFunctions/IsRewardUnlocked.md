---
title: "IsRewardUnlocked"
description: "Checks if a reward of the given type and name is unlocked."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Checks if a reward of the given type and name is unlocked.

# Syntax
```lua
IsRewardUnlocked( type, name )
```

## Arguments
* **type** (integer): The type of reward to check.
	* For convenience, constants for all valid reward types are provided in the [[../LuaTables/RewardType.md]] table.
* **name** (string): The name of the reward.

## Return Values
* (boolean): Whether the reward is unlocked.

# Examples
```lua
local ElectaurusUnlocked = IsRewardUnlocked(RewardType.Car, "elect_v")
if ElectaurusUnlocked then
	-- Do something if the Electaurus has been unlocked
end
```