---
title: "Redirect"
description: "Redirect the file being requested to a different path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Redirect the file being requested to a different path.

# Syntax
```lua
Redirect( path )
```

## Arguments
* **path** (string): The path to redirect this file to.

## Return Values
No return values.

# Examples
```lua
-- Example redirection to a random file in the Mod's Resources folder.
local FilePath = GetModPath() .. "/Resources/example/"

local Files = {"example.p3d","example2.p3d","example3.p3d"}

Redirect(FilePath .. Files[math.random(1, #Files)])
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}