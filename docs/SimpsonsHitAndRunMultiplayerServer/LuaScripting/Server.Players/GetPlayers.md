---
title: "Server.Players.GetPlayers"
description: "Provides information about the Server.Players.GetPlayers function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a table containing all currently connected players on the server.

# Syntax
```lua
Server.Players.GetPlayers()
```

## Arguments
No arguments.

## Return Values
* (table): A table of all connected [[../../DataStructures/Player.md]] objects.

# Examples
```lua
local players = Server.Players.GetPlayers()
for i = 1, #players do
    local player = players[i]
    print(player.Name)
end
```
