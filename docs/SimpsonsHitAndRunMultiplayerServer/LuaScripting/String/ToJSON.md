---
title: "String.ToJSON"
description: "Provides information about the String.ToJSON function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
---

Converts a Lua table to a JSON string.

**Added in Version 1.1.**

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
