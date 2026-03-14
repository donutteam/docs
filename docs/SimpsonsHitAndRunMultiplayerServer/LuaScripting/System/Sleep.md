---
title: "System.Sleep"
description: "Provides information about the System.Sleep function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Pauses execution of the current script for a specified duration. Suspends the calling context and resumes it automatically after `delay` milliseconds have elapsed.

# Syntax
```lua
System.Sleep( delay )
```

## Arguments
* **delay** (number): The duration to sleep in milliseconds.

## Return Values
No return values.

# Examples
```lua
print("Sleeping for 2 seconds...")
System.Sleep(2000)
print("Awake now!")
```
