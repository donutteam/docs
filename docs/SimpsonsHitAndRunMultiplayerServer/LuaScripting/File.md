---
title: "File"
description: "Provides information about the File table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `File` table provides functions for performing file operations in Simpsons Hit & Run Multiplayer Server mods.

The `File` table is restricted to your mod's directory (e.g., `./Mods/YourMod/`) and cannot access files outside of this directory for security reasons.

## Variables
This table does not have any variables.

## Methods

| Function Name           | Description                                                      |
|-------------------------|------------------------------------------------------------------|
| [[File/Exists.md]]      | Checks if a file exists at the specified path.                   |
| [[File/ReadAll.md]]     | Reads the entire content of a file.                              |
| [[File/ReadOffset.md]]  | Reads a portion of a file starting from a specific offset.       |
| [[File/Require.md]]     | Requires a file, executing it if it hasn't been executed before. |
| [[File/RequireOnce.md]] | Requires a file, executing it only once.                         |
| [[File/Write.md]]       | Writes content to a file.                                        |
| [[File/Delete.md]]      | Deletes a file at the specified path.                            |