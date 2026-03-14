---
title: "Server.TriggerEvent"
description: "Provides information about the Server.TriggerEvent function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Triggers a specified event with optional arguments. This can be used to trigger custom events that other scripts, or mods, can listen for using [[AddEventListener.md]].

# Syntax
```lua
Server.TriggerEvent( event, ... )
```

## Arguments
* **event** (string): The name of the event to trigger.
* **...** (any): Optional arguments to pass to the event listeners.

## Return Values
No return values.

# Examples
```lua
Server.TriggerEvent("MyCustomEvent", {
    Message = "Hello, world!",
    Number = 42
})
```