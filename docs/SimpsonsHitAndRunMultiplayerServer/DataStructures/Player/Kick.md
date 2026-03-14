---
title: "Player:Kick"
description: "Provides information about the Player:Kick function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Kicks the player from the server.

# Syntax
```lua
Player:Kick( [ message ] )
```
 
## Arguments
* **message** (string, optional): An optional message to display to the player when they are kicked.

## Return Values
No return values.

# Examples
```lua
local player = --[[ get player reference ]]
player:Kick("This isn't Donut SMP.")
```