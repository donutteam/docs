---
title: "PlayerCharacter:GetPosition"
description: "Provides information about the PlayerCharacter:GetPosition function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Gets the player's character's current position in the level. This is `nil` if the player is not currently in a level.

# Syntax
```lua
Character:GetPosition()
```

## Arguments
No arguments.

## Return Values
* `position` ([[../../LuaScripting/Engine.Vector3.md|Vector3]] or `nil`) - The player's character's current position in the level, or `nil` if the player is not currently in a level.

# Examples
```lua
local success, result = Server.Players.GetPlayer(playerName)
if not success then
    -- Handle error
    return
end

local position = result.Character:GetPosition()
```