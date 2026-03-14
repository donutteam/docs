---
title: "DB.LastInsertId"
description: "Provides information about the DB.LastInsertId function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns the ID of the last row that was inserted into the database.

# Syntax
```lua
DB.LastInsertId()
```

## Arguments
No arguments.

## Return Values
(number): The ID of the last row that was inserted into the database. If no rows have been inserted, this will return 0.

## Examples
```lua
DB.Execute([[
    INSERT INTO users (username, password_hash, operator)
    VALUES (@username, @password_hash, 1);
]],
{
    username = "maz_likes_eggs",
    password_hash = Cryptography.SHA256("super_secure_password")
})

local lastId = DB.LastInsertId()
print(lastId) -- Outputs: 1 (example output, will vary based on the actual last inserted ID)
```