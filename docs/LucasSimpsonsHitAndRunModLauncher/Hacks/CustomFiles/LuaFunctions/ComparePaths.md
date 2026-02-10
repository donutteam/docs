---
title: "ComparePaths"
description: "Compares two paths with options to ignore different casing and different slashes."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Compares two paths with options to ignore different casing and different slashes.

# Syntax
```lua
ComparePaths( path1, path2, [case_insensitive, slash_insensitive] )
```

## Arguments
* **path1** (string): The first path.
* **path2** (string): The second path.
* **case_insensitive** (boolean): Whether or not the comparison is case insensitive. 
    * Optional, defaults to true.
* **slash_insensitive** (boolean): Whether or not the comparison is slash insensitive. 
    * Optional, defaults to true.

## Return Values
* (boolean): Whether the paths match.

# Examples
```lua
-- Result is true
local Result = ComparePaths("art\\cars\\famil_v.p3d", "art/cars/famil_v.p3d")

-- Result is false, the capitalization is different.
local Result = ComparePaths("ART\\CARS\\FAMIL_V.p3d", "art/cars/famil_v.p3d", false)

-- Result is false, the slashes are different.
local Result = ComparePaths("ART\\CARS\\FAMIL_V.p3d", "ART/CARS/FAMIL_V.p3d", true, false)
```

# Version History
## Version 1.19
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/CustomFiles/LuaFunctions/ComparePaths.md }}