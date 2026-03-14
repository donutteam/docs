---
title: "String.GUID"
description: "Provides information about the String.GUID function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Creates a new globally unique identifier (GUID) string.

# Syntax
```lua
String.GUID()
```

## Arguments
No arguments.

## Return Values
* (string): A new GUID string in the format.

# Examples
```lua
local guid = String.GUID()
print(guid) -- Example output: "3f2504e0-4f89-11d3-9a0c-0305e82c3301"
```