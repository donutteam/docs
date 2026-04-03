---
title: "String.ToJSON"
description: "Provides information about the String.ToJSON function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 528 # 1.1
---

Converts a Lua table to a JSON string.

# Syntax
```lua
String.ToJSON( table )
```

## Arguments
* `table` (table): The Lua table to convert to a JSON string. Nested tables are converted recursively.

## Return Values
* (string): A JSON string representation of the table.

# Examples
```lua
local json = String.ToJSON({ name = "Homer", level = 1 })
print(json) -- Outputs: {"name":"Homer","level":1}
```
