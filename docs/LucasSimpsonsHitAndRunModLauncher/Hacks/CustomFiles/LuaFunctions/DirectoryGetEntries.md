---
title: "DirectoryGetEntries"
description: "Calls a callback function for every file and sub-directory in the given path."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Calls a callback function for every file and sub-directory in the given path.

The order of these files is not predictable and should not be relied upon.

# Syntax
```lua
DirectoryGetEntries( path, callback, [end_to_start] )
```

## Arguments
* **path** (string): The directory to iterate.
* **callback** (function(FileOrDirectory, IsDirectory)): A callback that will be called for each item in the directory.
	* **FileOrDirectory** (string): The file or directory name.
	* **IsDirectory** (boolean): Whether **FileOrDirectory** refers to a directory.
	* This callback can return `true` to continue iteration. Returning any other value or not returning anything will end it.
* **end_to_start** (boolean): Makes the function iterate the directory in reverse order. 
    * Optional, defaults to false.

## Return Values
* (boolean): Whether the **callback** returned **true** every time.

# Examples
```lua
-- Print each file and whether or not it's a directory.
DirectoryGetEntries(Path, function(FileOrDirectory, IsDirectory)
    print(FileOrDirectory, IsDirectory)

    return true
end)
```

# Version History
## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/DirectoryGetEntries.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/CustomFiles/LuaFunctions/DirectoryGetEntries.md }}