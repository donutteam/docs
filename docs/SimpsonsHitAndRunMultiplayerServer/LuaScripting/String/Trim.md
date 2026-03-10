---
title: "String.Trim"
description: "Provides information about the String.Trim function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Removes leading and trailing whitespace from a string.

# Syntax
```lua
String.Trim( input )
```

## Arguments
* `input` (string): The string to be trimmed.

## Return Values
* (string): The trimmed string.

# Examples
```lua
local result = String.Trim("   Hello, world!   ")
print(result)  -- Output: "Hello, world!"
```