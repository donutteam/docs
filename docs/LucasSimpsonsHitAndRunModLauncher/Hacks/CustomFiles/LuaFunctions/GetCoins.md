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
GetCoins()
```

## Arguments
No arguments.

## Return Values
* (integer | nil): The amount of coins the player currently has or `nil` if unavailable.

# Examples
```lua
local Coins = GetCoins()
if Coins == 69 then
	print("Nice.")
elseif Coins == 73 then
	print("LMAOOOO")
end
```