---
title: "String.Contains"
description: "Provides information about the String.Contains function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a string contains a specified substring.

# Syntax
```lua
String.Contains( input, substring, [ comparisonType ] )
```

## Arguments
* `input` (string): The string to be checked.
* `substring` (string): The substring to check for within the string.
* `comparisonType` ([[StringComparison.md]], optional): The type of string comparison to perform. Defaults to `Ordinal`.

## Return Values
* (boolean): `true` if the string contains the specified substring, `false` otherwise.

# Examples
```lua
local result = String.Contains("I hate the world!", "hate")
if result then
    -- Ban the pessimist for spreading negativity!
else
    -- They aight.
end
```