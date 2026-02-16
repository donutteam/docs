---
title: "GetCustomSaveDataValues"
description: "Gets all custom save data values for a mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets a custom save data value for a mod.

# Syntax
```lua
GetCustomSaveDataValues( [mod_name] )
```

## Arguments
* **mod_name** (string): The name of the mod to get the values from.
	* Optional, defaults to the current mod.

## Return Values
* (table<string, boolean | integer | number | string>): A key/value table of all the values for the given mod.

# Examples
```lua
local MyModsValues = GetCustomSaveDataValues()

local AnotherModsValues = GetCustomSaveDataValues("DonutMod")
```

# Notes
This function will throw an error if it is called before the game's save manager is available (such as in CustomFiles.lua).