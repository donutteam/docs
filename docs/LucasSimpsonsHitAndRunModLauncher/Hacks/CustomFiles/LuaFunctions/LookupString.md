---
title: "LookupString"
description: "Gets the current value for a string from the game's text bible."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets the current value for a string from the game's text bible.

# Syntax
```lua
LookupString( string_name )
```

## Arguments
* **string_name** (string): The name of a string.

## Return Values
* (string | nil): The current value of the string or `nil` if it cannot be found.

# Examples
```lua
local MissionObjective00 = LookupString("MISSION_OBJECTIVE_00")
```

# Notes
This looks up the current value of the string, including per level/mission overrides from the [[../../CustomText.md]] hack.