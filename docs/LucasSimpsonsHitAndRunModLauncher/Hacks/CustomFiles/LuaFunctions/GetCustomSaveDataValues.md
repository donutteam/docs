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
* (table<string, boolean | integer | number | string> | nil): A key/value table of all the values for the given mod or `nil` if the mod has no data in the save file.

# Examples
```lua
local MyModsValues = GetCustomSaveDataValues()
-- Do something with this mod's values

local AnotherModsValues = GetCustomSaveDataValues("DonutMod")
if AnotherModsValues ~= nil then
	-- Do something with the other mod's values.
end
```

# Notes
This function will throw an error if it is called before the game's save manager is available (such as in CustomFiles.lua).