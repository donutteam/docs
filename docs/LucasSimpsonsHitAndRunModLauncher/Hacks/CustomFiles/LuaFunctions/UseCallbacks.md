---
title: "UseCallbacks"
description: "Builds a file as the game requests it using callback functions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Builds a file as the game requests it using callback functions.

# Syntax
```lua
UseCallbacks( length, read_callback, close_callback )
```

## Arguments
* **length** (integer): The file size of the file in bytes.
* **read_callback** (fun(position, length)): Callback called each time the game tries to read from the file.
	* **position** (integer): The position the game is reading from.
	* **length** (integer): How much data the game is trying to read.
* **close_callback** (fun()): Callback called when the game closes its handle on the file.

## Return Values
No return values.

# Examples
Don't fucking use this.

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}