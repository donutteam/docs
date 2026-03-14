---
title: "IsLegacyOutput"
description: "Checks whether or not the -legacyoutput command line argument is in use."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 402 # 1.23.9
---

Checks whether or not the `-legacyoutput` [[../../../CommandLineArguments.md|command line argument]] is in use.

# Syntax
```lua
IsLegacyOutput()
```

## Arguments
No arguments.

## Return Values
* (boolean): Whether the `-legacyoutput` [[../../../CommandLineArguments.md|command line argument]] is in use.

# Examples
```lua
local IsLegacyOutput = IsLegacyOutput()
```