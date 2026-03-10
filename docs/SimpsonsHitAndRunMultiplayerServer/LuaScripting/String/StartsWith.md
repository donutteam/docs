---
title: "String.StartsWith"
description: "Provides information about the String.StartsWith function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Checks if a string starts with a specified substring.

# Syntax
```lua
String.StartsWith( input, substring )
```

## Arguments
* `input` (string): The string to be checked.
* `substring` (string): The substring to check for at the start of the string.

## Return Values
* (boolean): `true` if the string starts with the specified substring, `false` otherwise.

# Examples
```lua
local result = String.StartsWith("Hello, world!", "Hello")
if result then
    print("The string starts with 'Hello'")
else
    print("The string does not start with 'Hello'")
end
```