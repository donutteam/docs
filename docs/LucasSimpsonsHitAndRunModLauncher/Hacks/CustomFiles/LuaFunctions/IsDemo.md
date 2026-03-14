---
title: "IsDemo"
description: "Checks if the user is playing the demo version of the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 403 # 1.23.10
---

Checks if the user is playing the demo version of the game.

# Syntax
```lua
IsDemo()
```

## Arguments
No arguments.

## Return Values
* (boolean): Whether the user is playing the demo version of the game.

# Examples
```lua
if IsDemo() then
	-- Do demo specific stuff
end
```