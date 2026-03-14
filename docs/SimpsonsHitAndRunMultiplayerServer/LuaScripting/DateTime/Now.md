---
title: "DateTime.Now"
description: "Provides information about the DateTime.Now function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns the total seconds since January 1, 1970 (Unix epoch) as a number.

# Syntax
```lua
DateTime.Now()
```

## Arguments
No arguments.

## Return Values
(number): The total seconds since January 1, 1970 (Unix epoch).

# Examples
```lua
local currentTime = DateTime.Now()
print(currentTime) -- Outputs: 1625159073 (example output, will vary based on current time)
```