---
title: "WildcardMatch"
description: "Checks if text matches the given wildcard string."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 355 # 1.8
---

Checks if text matches the given wildcard string.

# Syntax
```lua
WildcardMatch( text, wildcard, case_insensitive, slash_insensitive )
```

## Arguments
* **text** (string): The text to compare against the wildcard.
* **wildcard** (string): The wildcard string to compare against.
	* Use `*` to match zero or more of any character.
	* Use `?` to match one of any character.
* **case_insensitive** (boolean): Whether or not the comparison is case insensitive.
* **slash_insensitive** (boolean): Whether or not the comparison is slash insensitive.

## Return Values
* (boolean): Whether the **text** matched the **wildcard**.

# Examples
```lua
local Path = GetPath()

-- Will match paths like:
--	sound/scripts/level1.spt
--	sound\scripts\level2.spt
--	SOUND\SCRIPTS\LEVEL3.SPT
--  SoUnD/ScRiPtS/LeVeL4.SpT
--
-- But not something like
--	sound/scripts/level01.spt
if WildcardMatch(Path, "sound/scripts/level?.spt", true, true) then
	-- Do stuff if Path matches
end

-- This, however, will match paths like:
--	sound/scripts/level1.spt
--	sound/scripts/level01.spt
--	SOUND\SCRIPTS\LEVEL000001.spt
if WildcardMatch(Path, "sound/scripts/level*.spt", true, true) then
	-- Do stuff if Path matches
end
```