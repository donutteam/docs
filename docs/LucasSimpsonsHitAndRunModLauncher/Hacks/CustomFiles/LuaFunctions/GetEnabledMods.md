---
title: "GetEnabledMods"
description: "Calls the given callback function for each mod that is enabled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Calls the given callback function for each mod that is enabled.

# Syntax
```lua
GetEnabledMods( callback )
```

## Arguments
* **callback** function(ModInternalName): A callback that will be called for each enabled mod.
	* **ModInternalName** (string): The InternalName of the mod.
	* This callback can return `true` to continue iteration. Returning any other value or not returning anything will end it.

## Return Values
* (boolean): Whether the **callback** returned **true** every time.

# Examples
```lua
-- Print the InternalName of each enabled mod/hack
GetEnabledMods(function(ModInternalName) 
	print(ModInternalName)
	return true
end)
```