---
title: "File.Require"
description: "Provides information about the File.Require function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Executes a Lua file.

# Syntax
```lua
File.Require( path )
```

## Arguments
* **path** (string): The path of the file to execute.

## Return Values
* (boolean): Returns true if the file was successfully executed, or false if the file does not exist or an error occurred during execution.

# Examples
```lua
local result = File.Require("path/to/another_script.lua")
if result then
    print("File executed successfully!")
else
    print("Failed to execute file.")
end
```