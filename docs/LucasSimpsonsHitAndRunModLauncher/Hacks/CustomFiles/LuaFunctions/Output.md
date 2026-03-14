---
title: "Output"
description: "Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested.

Calling this function multiple times within the same path handler will cause the data to be concatenated.

# Syntax
```lua
Output( data )
```

## Arguments
* **data** (string): The data to output to the virtual file.

## Return Values
No return values.

# Examples
```lua
-- Example that would be used in a PathHandler on an MFK script
Output([[
    LoadP3DFile("art\\cars\\famil_v.p3d");
]])
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/CustomFiles/LuaFunctions/Output.md }}