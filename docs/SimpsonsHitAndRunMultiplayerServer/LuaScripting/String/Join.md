---
title: "String.Join"
description: "Provides information about the String.Join function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Joins a table of substrings into a single string using a specified delimiter.

# Syntax
```lua
String.Join( input, glue )
```

## Arguments
* `input` (table): The table of substrings to be joined.
* `glue` (string): The delimiter to use for joining the substrings.

## Return Values
* (string): A single string resulting from joining the substrings with the specified delimiter.

# Examples
```lua
local joinedString = String.Join({"I", "am", "evil", "Homer"}, " ")
print(joinedString) -- Outputs: "I am evil Homer"
```