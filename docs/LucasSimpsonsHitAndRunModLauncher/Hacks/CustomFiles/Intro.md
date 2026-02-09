---
title: "Introduction"
description: "This hack allows mods to provide custom files without modifying the game install."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to provide custom files without modifying the game install.

It also allows mods to handle the game requesting files with Lua scripts which allows for a number of powerful features.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomFiles
```

Your mod must provide at least one of the following things when requiring this hack:

* `CustomFiles.ini`
* `CustomFiles.lua`
* A `CustomFiles` folder.
* An `AdditionalFiles` folder.

# Configuring This Hack
To configure this hack, create a file named `CustomFiles.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
; OccludedPath
; 	Occlude a file from the game's view, this will make the game think it doesn't exist. Be careful with this. 
; 	Repeatable to occlude multiple files.
OccludedPath=path\\to\\file.p3d

; ReadOnly
; 	Prevents the game from writing to a file, but it can still read it. 
; 	Repeatable to make multiple files read only.
ReadOnly=path\\to\\file.p3d

; SuppressedPath
; 	Tries to prevent the game from loading a file. 
; 	Repeatable to suppress multiple files.
SuppressedPath=path\\to\\file.p3d
	
[PathRedirections]
; PATH_TO_FILE
; 	Redirect the file on the left to the path on the right.
;	Repeatable to redirect multiple files.
art\\frontend\\dynaload\\images\\license\\*.p3d=art\\license\\license.p3d

[PathHandlers]
; PATH_TO_FILE
; 	Specify a file path that, when requested, will cause a Lua Path Handler script to be executed.
; 	Repeatable to handle multiple files.
art\\cars\\family_v.p3d=Resources/scripts/handlers/famil_v.lua

[AdditionalFiles]
; PATH_TO_FILE
; 	Specify a file on the right that will also be loaded when the left file is loaded.
;	Repeatable for the same base file or for any number of different files.
art\\cars\\famil_v.p3d=art\\cars\\famil_vH.p3d
```

\* Wildcard can be used in a path to indicate anything of any length.
? Wildcard can be used in a path to indicate anything of a set length.

# Folders
## CustomFiles
The main folder for this hack is one called "CustomFiles". This folder allows mods to override files in the base game. 

For example, a mod with a custom version of the Family Sedan at the path `CustomFiles\art\cars\famil_v.p3d` will override the game's original model for it.

## AdditionalFiles
Mods can also use a folder named "AdditionalFiles" is similar to "CustomFiles" but instead of overriding the files, it makes the game load the original file and the custom file. 

This functionality can break the game in a number of cases such as when it is used on a sound script (`.spt`).

## Resources
Lastly, mods that use this hack's [[LuaScripting.md]] capabilities are expected to use a folder named **Resources** for any Lua scripts (besides `CustomFiles.lua`) and any other files that are exclusively redirected to or read by Lua scripts.

# Lua Scripting
For more detailed information, see [[LuaScripting.md]].

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomFiles.md }}

## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomFiles.md }}

## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomFiles.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles.md }}

## Version 1.23.12
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.12/Hacks/CustomFiles.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/CustomFiles.md }}

## Version 1.23.8
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/CustomFiles.md }}

## Version 1.19
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/CustomFiles.md }}

## Version 1.13.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13.2/Hacks/CustomFiles.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles.md }}

## Version 1.12.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12.1/Hacks/CustomFiles.md }}

## Version 1.12
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12/Hacks/CustomFiles.md }}