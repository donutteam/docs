---
title: "IsWriting"
description: "Checks if the path being handled is being written to."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 358 # 1.10
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Checks if the path being handled is being written to.

# Syntax
```lua
IsWriting()
```

## Arguments
No arguments.

## Return Values
* (boolean): Whether the path being handled is being written to.

# Examples
```lua
if IsWriting() then
    -- Unsure what you could even do with this.
end
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}