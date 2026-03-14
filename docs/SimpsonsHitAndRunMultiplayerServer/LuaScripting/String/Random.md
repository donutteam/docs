---
title: "String.Random"
description: "Provides information about the String.Random function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Generates a random string of a specified length, optionally using a custom set of characters.

# Syntax
```lua
String.Random( length, [ chars ] )
```

## Arguments
* **length** (number): The length of the random string to generate.
* **chars** (string, optional): A string containing the characters to use for generating the random string. If not provided, a default set of alphanumeric characters will be used.

## Return Values
* (string): A new random string of the specified length.

# Examples
```lua
local randomString = String.Random(3)
print(randomString) -- Example output: "A1c"
```