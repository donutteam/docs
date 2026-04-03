---
title: "Server.Players.GetPlayersWhere"
description: "Provides information about the Server.Players.GetPlayersWhere function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a filtered table of currently connected players matching the given filter criteria. If no filters are provided, all players are returned.

# Syntax
```lua
Server.Players.GetPlayersWhere( filters, [ caseInsensitive ] )
```
## Arguments
* **filters** (table, optional): A table of key-value pairs to filter players by. Supported keys are:
  * **name** (string): Matches players by their name.
  * **discriminator** (string): Matches players by their discriminator.
  * **mainMod** (MainMod): Matches players by their selected main mod.
  * **session** ([[../Session.md|Session]]): Matches players by their session.
* **caseInsensitive** (boolean, optional): Whether string filters should be matched in a case-insensitive manner. Defaults to true.

## Return Values
* (table): A table of [[../../DataStructures/Player.md|Player]] objects matching all provided filters.

# Examples
```lua
local filters = { name = "loren" }
local players = Server.Players.GetPlayersWhere(filters, false)
for i = 1, #players do
    local player = players[i]
    player:Kick("Get back to work on Donut Mod, " .. player.Name .. "!")
end
```
