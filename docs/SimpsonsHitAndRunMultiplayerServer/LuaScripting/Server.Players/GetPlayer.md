---
title: "Server.Players.GetPlayer"
description: "Provides information about the Server.Players.GetPlayer function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Finds and returns a single player by name and discriminator. Can be called with a combined `PlayerName#Discriminator` string, or with the name and discriminator as two separate arguments.

# Syntax
```lua
Server.Players.GetPlayer( nameAndDiscriminator )
Server.Players.GetPlayer( name, discriminator )
```
## Arguments
* **nameAndDiscriminator** (string): The player's full identifier in the form `PlayerName#Discriminator`.

**or**

* **name** (string): The player's name.
* **discriminator** (string): The player's discriminator.


## Return Values
* (Player): The matching Player object if found.
* (boolean, string): Returns `false` and an error message string if the arguments are invalid or no matching player is found.


# Examples
```lua
local ok, result = Server.Players.GetPlayer("Homer#1234")
if ok then
    print(result.Name)
else
    print("Error: " .. result)
end

local ok2, result2 = Server.Players.GetPlayer("Homer", "1234")
if ok2 then
    print(result2.Name)
else
    print("Error: " .. result2)
end
```
