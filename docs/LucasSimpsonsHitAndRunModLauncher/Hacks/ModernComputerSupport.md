---
title: "Modern Computer Support"
description: "This hack makes various patches to the game to make it work better on modern computers and operating systems."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/AlwaysEnabled.md }}

This hack makes various patches to the game to make it work better on modern computers and operating systems.

# Features
This is a list of fixes that are applied by this hack.

* Fixes slow load times on Windows Vista / Windows Server 2003 or newer.
    * This hack does not do this if [[LoadManagerThreadCoordination.md]] is enabled as it is not necessary.
    * How this is achieved is dependent on whether or not "Limit to Single Core" is enabled on the "Game" tab of the [[../Settings.md|launcher's settings]].
        * If enabled, this is done by making any threads created by the game run on your first processor core.
        * If disabled, this hack will instead change various Sleep calls in the game to be called with a 1 instead of a 0.
	* This fix can be opted out of with the `-noslowfileloadfixes` [[../CommandLineArguments.md|command line argument]].
	* This fix can forced on with the `-forceslowfileloadfixes` [[../CommandLineArguments.md|command line argument]].
* Makes the game window get centered properly in Windowed mode if your screen resolution is wider than 1600 pixels.
* Makes the game work if it's installed to a drive with the letter `A:` or `B:`.
* Makes DirectSound's maximum sample rate 200,000hz instead of 100,000hz in non-English releases of the game.
    * The original English release already has a maximum of 200,000. This change is just to make it consistent.
* Makes it so the game cannot have a delta time of 0 by skipping any frames that would have resulted in that (which happens when the frame-rate goes over 1000).
    * This fixes issues where positions of various things like the player could become NaN (due to the game dividing by 0).
    * This fix can be opted out of with the `-allowzerodeltatime` [[../CommandLineArguments.md|command line argument]].
* Fixes an issue where you cannot bind mouse buttons when using a non-English Windows language.
	* This fix can be opted out of with the `-nononenglishwindowsmousebuttonfix` [[../CommandLineArguments.md|command line argument]].
* Fixes an issue where the game incorrectly centered the cursor to the window instead of it's client area *and* an issue where the game assumed the non-client area was 30 pixels at the top and 10 pixels at the other edges when clipping the cursor.
	* This fix can be opted out of with the `-noproperclientareacursorcentringandclipping` [[../CommandLineArguments.md|command line argument]].

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.26.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26.1/Hacks/ModernComputerSupport.md }}

## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/ModernComputerSupport.md }}

## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/ModernComputerSupport.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/ModernComputerSupport.md }}

## Version 1.19
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/ModernComputerSupport.md }}

## Version 1.18.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.3/Hacks/ModernComputerSupport.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/ModernComputerSupport.md }}

## Version 1.17.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.2/Hacks/ModernComputerSupport.md }}