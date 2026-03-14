---
title: "print_r"
description: "Provides information about the print_r function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Prints a table in a human-readable format. This function is useful for debugging purposes, allowing you to inspect the contents of a table.

# Syntax
```lua
print_r( object, [ depth ] )
```

## Arguments
* `object` (any) - The object to be printed.
* `depth` (number, optional) - The current depth of the table being printed. This is used internally for recursive calls and should not be provided by the user. Default is 0, and the maximum depth is 10.

## Return Values
No return values.

# Examples
```lua
local exampleTable = {
    name = "Homer",
    age = 39,
    occupation = "Nuclear Safety Inspector, most of the time",
}

print_r(exampleTable)

--[[ Output:
<LuaTable> {
  name: Homer
  age: 39
  occupation: Nuclear Safety Inspector, most of the time
}
--]]
```