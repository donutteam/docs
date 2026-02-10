---
title: "GetShared"
description: "Returns a table that is shared by all mods."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 403 # 1.23.10
---

Returns a table that is shared by all mods.

# Syntax
```lua
GetShared()
```

## Arguments
No arguments.

## Return Values
* (table<string, any>): The shared table.

# Examples
Store something in the table in one mod:
```lua
local Shared = GetShared()

Shared.Example = "Potato"
```

And then print it from another mod afterwards:
```lua
local Shared = GetShared()

print(Shared.Example) -- prints "Potato"
```