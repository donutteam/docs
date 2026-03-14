---
title: "ReadFileOffset"
description: "Read part of a file at the given path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 79 # 1.24
---

Read part of a file at the given path.

# Syntax
```lua
ReadFileOffset( path, offset, length )
```

## Arguments
* **path** (string): The path of the file to read.
* **offset** (integer): The offset in the file in bytes. This value is 1 based.
* **length** (integer): The amount of bytes to read.

## Return Values
* (string): The part of the file.

# Examples
```lua
-- Random example to read a small, probably useless, part of L1_TERRA
local FilePart = ReadFileOffset("/GameData/art/L1_TERRA.p3d", 657, 512)
```

# Notes
Reading past the end of the file will return a shorter amount than what you requested.