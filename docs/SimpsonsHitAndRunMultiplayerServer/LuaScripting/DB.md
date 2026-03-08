---
title: "DB"
description: "Provides information about the DB table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `DB` table provides functions for interacting with the SQLite database in Simpsons Hit & Run Multiplayer Server mods.

## Properties

| Property Name | Description                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| `DB.NULL`     | A special value that can be used to represent `NULL` in SQL queries when binding parameters. |

## Methods

| Function Name          | Description                                              |
|------------------------|----------------------------------------------------------|
| [[DB/Connect.md]]      | Establishes a connection to the SQLite database.         |
| [[DB/Disconnect.md]]   | Closes the connection to the SQLite database.            |
| [[DB/Execute.md]]      | Executes a SQL query on the SQLite database.             |
| [[DB/LastInsertId.md]] | Returns the ID of the last inserted row in the database. |
