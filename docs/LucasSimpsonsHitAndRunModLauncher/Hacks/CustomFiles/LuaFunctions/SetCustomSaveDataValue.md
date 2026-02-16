---
title: "SetCustomSaveDataValue"
description: "Sets a custom save data value for a mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Sets a custom save data value for a mod.

# Syntax
```lua
SetCustomSaveDataValue( value_name, value )
```

## Arguments
* **value_name** (string): The name of the value.
* **value** (boolean | integer | number | string): The value to store in the save data.
	* Other types, such as tables, will throw an error.

## Return Values
No return values.

# Examples
```lua
SetCustomSaveDataValue("Potato", "Salad")
```

# Notes
* This function will throw an error if it is called before the game's save manager is available (such as in CustomFiles.lua).
* It is not possible to set a value for another mod.