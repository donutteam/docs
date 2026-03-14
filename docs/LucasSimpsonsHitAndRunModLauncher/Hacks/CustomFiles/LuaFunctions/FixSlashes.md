---
title: "FixSlashes"
description: "Returns a version of the given path with modified slashes."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 355 # 1.8
---

Returns a version of the given path with modified slashes.

# Syntax
```lua
FixSlashes( path, [to_windows, from_windows])
```

## Arguments
* **path** (string): The path to modify.
* **to_windows** (boolean): Whether to convert the path to have back slashes (`\`).
* **from_windows** (boolean): Whether to convert the path to have forward slashes (`/`).

## Return Values
* (string): The fixed path.

# Examples
```lua
--- Returns "scripts/missions/level01/level.mfk"
local Path1 = FixSlashes("scripts\\missions\\level01\\level.mfk", false, true)

--- Returns "scripts\missions\level01\level.mfk"
local Path2 = FixSlashes("scripts/missions/level01/level.mfk", true, false)
```

# Notes
Only one of the 2nd and 3rd arguments should be set to true.