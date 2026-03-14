---
title: "GetCustomSaveDataValue"
description: "Gets a custom save data value for a mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets a custom save data value for a mod.

# Syntax
```lua
GetCustomSaveDataValue( value_name, [mod_name] )
```

## Arguments
* **value_name** (string): The name of the value.
* **mod_name** (string): The name of the mod to get the value from.
	* Optional, defaults to the current mod.

## Return Values
* (boolean | int | number | string | nil): The value or `nil` if it does not exist.

# Examples
```lua
local MyCustomValue = GetCustomSaveDataValue("Potato")
```

# Notes
This function will throw an error if it is called before the game's save manager is available (such as in CustomFiles.lua).