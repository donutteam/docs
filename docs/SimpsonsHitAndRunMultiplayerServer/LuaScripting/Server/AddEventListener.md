---
title: "Server.AddEventListener"
description: "Provides information about the Server.AddEventListener function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Adds a new event listener for a specified event.

# Syntax
```lua
Server.AddEventListener( event, callback )
```

## Arguments
* **event** (string): The name of the event to listen for. You can register anything here, however there are some predefined events that you can listen for. For more information, see [[../Events.md]].
* **callback** (function): The function to call when the event is triggered.

## Return Values
* (number): A unique identifier for the event listener, which can be used to remove the listener later with [[RemoveEventListener.md]].


# Examples
```lua
Server.AddEventListener("PlayerJoined", function(e)
    local player = e.Client

    player:SendGameChatMessage("Welcome to " .. Server.Config.ServerName .. "!")
end)
```