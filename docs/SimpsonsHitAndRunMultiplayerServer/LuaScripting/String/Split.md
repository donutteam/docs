---
title: "String.Split"
description: "Provides information about the String.Split function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Splits a string into a table of substrings based on a specified delimiter.

# Syntax
```lua
String.Split( input, delimiter )
```

## Arguments
* `input` (string): The string to be split.
* `delimiter` (string): The delimiter to use for splitting the string.

## Return Values
* (table): A table containing the substrings resulting from the split operation.

# Examples
```lua
local tokens = String.Split("My|name|is|Jake", "|")

print_r(tokens)
--[[ Output:
<LuaTable> {
  1: My
  2: name
  3: is
  4: Jake
}
]]
```