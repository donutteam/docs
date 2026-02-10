---
title: "ReadFile"
description: "Read the file at the given path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Read the file at the given path.

# Syntax
```lua
ReadFile( path )
```

## Arguments
* **path** (string): The path of the file to read.

## Return Values
* (string): The contents of the file.

# Examples
```lua
local RewardsScript = ReadFile("/GameData/scripts/missions/rewards.mfk")
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/ReadFile.md }}