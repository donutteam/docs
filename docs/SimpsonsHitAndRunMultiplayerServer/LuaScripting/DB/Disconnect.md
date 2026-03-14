---
title: "DB.Disconnect"
description: "Provides information about the DB.Disconnect function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Closes the connection to the SQLite database. This function should be called when you are finished performing database operations to free up resources.

# Syntax
```lua
DB.Disconnect()
```

## Arguments
No arguments.

## Return Values
No return values.

# Examples
```lua
DB.Disconnect() 
-- After disconnecting, the database connection is closed and resources are freed.
```