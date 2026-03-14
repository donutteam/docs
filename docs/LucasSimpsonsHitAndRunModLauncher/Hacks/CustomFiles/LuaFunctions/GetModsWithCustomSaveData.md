---
title: "GetModsWithCustomSaveData"
description: "Gets a table of mods that have custom save data in the current save file."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Gets a table of mods that have custom save data in the current save file.

# Syntax
```lua
GetModsWithCustomSaveData()
```

## Arguments
No arguments.

## Return Values
* (string[]): A table of mod names.

# Examples
```lua
local ModNames = GetModsWithCustomSaveData()
for i = 1, #ModNames do
	local ModName = ModNames[i]
	-- Do something with the mod name!
end
```

# Notes
This function will throw an error if it is called before the game's save manager is available (such as in CustomFiles.lua).