---
title: "GetLauncherVersion"
description: "Returns the current version of the Mod Launcher."
authors: [ 2, 395, 6310 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Returns the current version of the Mod Launcher as a string.

# Syntax
```lua
GetLauncherVersion()
```

## Arguments
No arguments.

## Return Values
* (string): The version number of the mod launcher.

# Examples
```lua
-- Separates a version string into a table of numbers.
function GetVersionParts(Version)
	local tbl = {}
	
    for part in Version:gmatch("[^%.]+") do
       tbl[#tbl + 1] = tonumber(part)
	end
	
    return tbl
end

-- Compares version table.
-- Returns positive is Version1 is newer, negative is Version1 is older or 0 if equal.
function CompareVersion(Version1, Version2)
	local Part1, Part2
	
    for i = 1, math.max(#Version1, #Version2) do
        Part1 = Version1[i] or 0
        Part2 = Version2[i] or 0
        
        if Part1 < Part2 then return -1 end
        if Part1 > Part2 then return 1 end
	end
	
    return 0
end

local LauncherVersion = GetLauncherVersion()

-- IsOldVersion will be true if launcher version is before 1.23.9
IsOldVersion = CompareVersion(GetVersionParts(LauncherVersion), {1, 23, 9}) < 0
```