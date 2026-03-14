---
title: "Server.RemoveEventListener"
description: "Provides information about the Server.RemoveEventListener function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Removes an event listener by its unique identifier.

# Syntax
```lua
Server.RemoveEventListener( listenerId )
```

## Arguments
* **listenerId** (number): The unique identifier of the event listener to remove.

## Return Values
No return values.


# Examples
```lua
local listenerId = Server.AddEventListener("PlayerJoined", function(e)
    -- ... event handling code ...
end)

Server.RemoveEventListener(listenerId)
```