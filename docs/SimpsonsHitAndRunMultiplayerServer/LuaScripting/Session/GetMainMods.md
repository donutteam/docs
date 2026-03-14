---
title: "Session.GetMainMods"
description: "Provides information about the Session.GetMainMods function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Retrieves all main mods that have been added by joined players.

# Syntax
```lua
Session.GetMainMods()
```

## Arguments
No arguments.

## Return Values
* (table): A table where the keys are the unique identifiers of the main mods.


# Examples
```lua
local mainMods = Session.GetMainMods()
for id, mod in pairs(mainMods) do
    print(id)
end
```