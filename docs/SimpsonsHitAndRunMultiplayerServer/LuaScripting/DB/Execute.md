---
title: "DB.Execute"
description: "Provides information about the DB.Execute function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Executes a SQL query on the SQLite database. This function can be used to perform various database operations such as creating tables, inserting data, updating records, and deleting records.

# Syntax
```lua
DB.Execute( query, [parameters] )
```

## Arguments
* **query** (string): The SQL query to execute. This can be any valid SQL statement such as `CREATE TABLE`, `INSERT INTO`, `UPDATE`, `DELETE`, etc.
* **parameters** (table, optional): A table of parameters to bind to the query. This is useful for preventing SQL injection attacks when inserting user-provided data into the database. The keys in the table should correspond to the parameter names in the query (e.g., `@username`, `@password_hash`), and the values should be the corresponding values to bind.
    * **Important:** You must use `DB.NULL` instead of passing `nil` for any parameters that should be set to `NULL` in the database.

## Return Values
No return values.

# Examples
```lua
DB.Execute([[
    INSERT INTO users (username, password_hash, operator)
    VALUES (@username, @password_hash, 1);
]],
{
    username = "maz_likes_eggs",
    password_hash = Cryptography.SHA256("super_secure_password")
})
```