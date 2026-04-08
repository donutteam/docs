---
title: "GetSetting"
description: "Returns the value of a setting in a mod."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Returns the value of a setting in a mod.

# Syntax
```lua
GetSetting( setting_name, [mod_name] )
```

## Arguments
* **setting_name** (string): The name of the setting to get the value of.
* **mod_name** (string): The mod you want to get the setting from.
	* Optional, defaults to the mod that called the function.

## Return Values
* (boolean | integer | number | string | nil): The value of the setting.
	* The type depends on the `Type` of the `[Setting]`.
	* Returns `nil` if the setting does not exist or no such mod is loaded.

# Examples
```lua
-- Get the difficulty setting of the current mod.
local Difficulty = GetSetting("Difficulty")

-- Check some other setting in another mod.
local SomeOtherSetting = GetSetting("SomeOtherSetting", "AnotherMod")
```

# Version History
## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/GetSetting_GetSettings.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/GetSetting.md }}

## Version 1.12.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12.1/Hacks/CustomFiles/LuaFunctions/GetSetting.md }}
