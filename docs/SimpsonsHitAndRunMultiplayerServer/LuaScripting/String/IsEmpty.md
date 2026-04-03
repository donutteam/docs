---
title: "String.IsEmpty"
description: "Provides information about the String.IsEmpty function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a string is empty or contains only whitespace characters.

# Syntax
```lua
String.IsEmpty( string )
```

## Arguments
* **string** (string | nil): The string to check.

## Return Values
* (boolean): `true` if the string is empty or contains only whitespace characters, `false` otherwise.

# Examples
```lua
local emptyString = ""
print(String.IsEmpty(emptyString)) -- Example output: true

local whitespaceString = "   "
print(String.IsEmpty(whitespaceString)) -- Example output: true

local nonEmptyString = "Hello"
print(String.IsEmpty(nonEmptyString)) -- Example output: false
```