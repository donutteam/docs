---
title: "File.Require"
description: "Provides information about the File.RequireOnce function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Executes a Lua file. If the same file is required again, it will not be executed again.

# Syntax
```lua
File.RequireOnce( path )
```

## Arguments
* **path** (string): The path of the file to execute.

## Return Values
* (boolean): Returns true if the file was successfully executed, or false if the file does not exist or an error occurred during execution.

# Examples
```lua
local result = File.RequireOnce("path/to/another_script.lua")
if result then
    print("File executed successfully!")
else
    print("Failed to execute file.")
end
```