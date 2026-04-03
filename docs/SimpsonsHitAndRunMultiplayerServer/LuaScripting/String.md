---
title: "String"
description: "Provides information about the String table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `String` table provides functions for working with strings.;

## Variables
| Variable Name                  | Description                                            |
|--------------------------------|--------------------------------------------------------|
| [[String/StringComparison.md]] | An enumeration for specifying string comparison types. |

## Methods
| Function Name            | Description                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------|
| [[String/Contains.md]]   | Checks if a string contains a specified substring.                                            |
| [[String/EndsWith.md]]   | Checks if a string ends with a specified substring.                                           |
| [[String/GUID.md]]       | Generates a globally unique identifier (GUID) as a string.                                    |
| [[String/IsEmpty.md]]    | Checks if a string is empty or `nil`.                                                         |
| [[String/Join.md]]       | Joins a table of substrings into a single string using a specified delimiter.                 |
| [[String/Random.md]]     | Generates a random string of a specified length, optionally using a custom set of characters. |
| [[String/Split.md]]      | Splits a string into a table of substrings based on a specified delimiter.                    |
| [[String/StartsWith.md]] | Checks if a string starts with a specified substring.                                         |
| [[String/ToJSON.md]]     | Converts a Lua table to a JSON string.                                                        |
| [[String/Trim.md]]       | Trims whitespace from the beginning and end of a string.                                      |
