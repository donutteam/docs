---
title: "GetGameLanguage"
description: "Returns the current language of the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 78 # 1.25
---

This function returns the current language of the game.

# Syntax
```lua
GetGameLanguage()
```

## Arguments
No arguments.

## Return Values
* (string): A letter indicating what language is in use.
	* **E**: If the game is in English.
	* **F**: If the game is in French.
	* **G**: If the game is in German.
	* **S**: If the game is in Spanish.

# Examples
```lua
local Language = GetGameLanguage()

if Language == "E" then
	-- Do stuff if the game is English
else
	-- Do other stuff if not
end
```

# Notes
This is affected by the user's game executable as well as by the Mod Launcher's `-language` [[../../../CommandLineArguments.md|command line argument]].