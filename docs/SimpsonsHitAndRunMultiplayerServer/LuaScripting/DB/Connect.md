---
title: "DB.Connect"
description: "Provides information about the DB.Connect function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Establishes a connection to the SQLite database. If a database file does not exist, it will be created automatically. This function must be called before performing any database operations.

# Syntax
```lua
DB.Connect()
```

## Arguments
No arguments.

## Return Values
No return values.

# Examples
```lua
DB.Connect() 
-- After connecting, you can perform database operations such as creating tables, inserting data, etc.
```