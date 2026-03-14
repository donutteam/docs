---
title: "GetCurrentSkin"
description: "Gets what skin the player is currently using."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets what skin the player is currently using.

# Syntax
```lua
GetCurrentSkin()
```

## Arguments
No arguments.

## Return Values
* (string | nil): The name of the skin the player is currently using or `nil` if the player is not in game.

# Examples
```lua
local CurrentSkin = GetCurrentSkin()
if CurrentSkin == "h_fat" then
	-- Do something if Homer is a fatass
end
```