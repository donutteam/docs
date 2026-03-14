---
title: "GetPath"
description: "Returns the path of the file being handled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Returns the path of the file being handled.

# Syntax
```lua
GetPath()
```

## Arguments
No arguments.

## Return Values
* (string): The path of the file being handled.

# Examples
```lua
local CurrentPath = GetPath()

if ComparePaths(CurrentPath, "scripts\\missions\\rewards.mfk") then
    -- Do something based on it being the rewards file.
else
    -- Do something else, nothing probably with this example
end
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}