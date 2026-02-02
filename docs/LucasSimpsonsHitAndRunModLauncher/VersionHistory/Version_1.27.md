---
title: "Version 1.27"
description: "Changelog for Version 1.27 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

# Launcher
## General
* Made the Mod Launcher itself respect the `-nocarindexmapping` command line argument during conflict checking.
* Fixed an issue that prevented encrypted mods from loading.
* Updated the Mod Launcher's copyright information.
* Potentially fixed various crashes related to jump lists.
* Improved the dialogue shown when compiling mods to list more details about what was compiled.
* Added a warning on startup if the Mod Launcher detects the game is installed within a cloud directory.
	* This currently attempts to detect Dropbox, Google Drive, OneDrive and iCloud.
	* This can be disabled with the new **Warn on Cloud Directories** setting in Launcher settings.
* Removed `lucasstuff.com` from the list of valid Donut Team URLs.
	* This affects the obscure `-apiurl` and obscure `-updatecheckurl` [[../CommandLineArguments.md]] that pretty much only exist for internal testing.
* Changed the encoding used when reading text files from ANSI to UTF8.
* Made it so, when loading mods, `[PathHandlers]` in `CustomFiles.ini` are validated to ensure that the handler script exists.

## Main Window
* Made it so the **Launch** button is now disabled when the game is attempting to launch and re-enabled when this either succeeds or fails.
* Made it so when Multiplayer is enabled the **Launch** will instead read **Play Multiplayer**.
* Redesigned the main window with a tool strip at the top, containing **File**, **View** and **Help** menus.
	* This tool strip replaces the **Open...** and **Account...** buttons, previously found on the main window, to follow a more universally understood design for programs.
* Fixed a bug where right clicking a mod setting hack that's also requirable by mods and choosing **Copy Require Line** would copy `RequiredMod=HackName` instead of `RequiredHack=HackName`.

## About Window
Added this new window that can be accessed from **Help** > **About...** on the main window's new tool strip.

The **Licenses** tab, previously located on the Launcher Settings window, has also now been moved to this new window.
