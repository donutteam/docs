---
title: "GetCoins"
description: "Gets the amount of coins the player currently has."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the amount of coins the player currently has.

# Syntax
```lua
GetCoins( [level] )
```

## Arguments
* **level** (integer): The level to get the coin count for.
	* Optional, defaults to 1.
	* By default, all levels share a coin count, however, the [[../../PerLevelCoinCount.md]] hack may be in use which can make this return different values depending on the level.

## Return Values
* (integer | nil): The amount of coins the player currently has in the specified level or `nil` if unavailable.

# Examples
```lua
local Coins = GetCoins()
if Coins == 69 then
	print("Nice.")
elseif Coins == 73 then
	print("LMAOOOO")
end
```