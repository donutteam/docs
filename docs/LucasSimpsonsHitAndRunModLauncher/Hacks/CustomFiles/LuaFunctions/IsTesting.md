---
title: "IsTesting"
description: "Checks whether the -testing command line argument is in use."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Checks whether the `-testing` [[../../../CommandLineArguments.md|command line argument]] is in use.

# Syntax
```lua
IsTesting()
```

## Arguments
No arguments.

## Return Values
* (boolean): Whether the `-testing` [[../../../CommandLineArguments.md|command line argument]] is in use.

# Examples
```lua
local IsTestingLauncher = IsTesting()
```