---
title: "DateTime.Date"
description: "Provides information about the DateTime.Date function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a formatted date string based on the provided format string and the current date and time.

# Syntax
```lua
DateTime.Date( format, [ epoch ] )
```

## Arguments
* **format** (string): A format string that specifies how the date should be formatted. It uses the .NET date and time format specifiers. For example, "yyyy-mm-dd HH:MM:SS" would format the date as "2021-01-01 12:34:56".
  * For more information on the available format specifiers, see the .NET documentation: https://docs.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings
* **epoch** (number, optional): An optional Unix timestamp (number of seconds since January 1, 1970) to format. If not provided, the current date and time will be used.

## Return Values
(string): The formatted date string.

# Examples
```lua
local formattedDate = DateTime.Date("yyyy-mm-dd HH:MM:SS")
print(formattedDate) -- Outputs: 2026-01-01 12:34:56 (example output, will vary based on current date and time)

local formattedDateFromEpoch = DateTime.Date("yyyy-mm-dd HH:MM:SS", 1609459200)
print(formattedDateFromEpoch) -- Outputs: 2021-01-01 00:00:00
```