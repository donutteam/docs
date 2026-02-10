---
title: "IsModEnabled"
description: "Checks whether or not a mod, mod hack or framework is enabled."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Checks whether or not a mod, mod hack or framework is enabled.

# Syntax
```lua
IsModEnabled( mod_name )
```

## Arguments
* **mod_name** (string): The name of the mod to check for. This should be the mod's InternalName (if it has one, which it should).

## Return Values
* (boolean): Whether the mod, mod hack or framework is enabled.

# Examples
```lua
if IsModEnabled("ReplayableBonusMissions") then
    -- Do stuff differently if the Replayable Bonus Missions Mod Hack is enabled.
end
```

# Version History
## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/IsModEnabled.md }}