---
title: Hack Support
description: "This hack manages and co-ordinates all other hacks, provides shared patches/functionality to hacks, loads mods and provides the underlying virtual file system used by Mods and Hacks."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/AlwaysEnabled.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByModToBeConfigured.md }}

This hack manages and co-ordinates all other hacks, provides shared patches/functionality to hacks, loads mods and provides the underlying virtual file system used by Mods and Hacks.

While Hack Support provides shared patches to other hacks, it only patches the game with the ones that are necessary for the loaded hacks as of Version 1.22.

# Features
These are features and changes provided by this hack.

* Adds various debug pages to [[DebugText.md]] if it's enabled.
* Changes the game's file not found message to [show a path and a retry button](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/FileNotFound.png) instead of just a [file name](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/FileNotFoundOriginal.png).
    * This can be opted out of through a couple different means:
        * As of version 1.23, you can use the `-nohandlefilenotfound` [[../CommandLineArguments.md|command line argument]].
        * Enabling Debug Test and then enabling its **No Handle File Not Found** setting on the **Miscellaneous** page of its Mod Settings.
* Changes the title of the games window and the icon based on enabled mods.
    * The icon is changed to that of the current Main mod (if it has an icon) or if to the icon of a mod with an Edition specified (if there's no Main mod with an icon).
    * The title is prefixed with the title of the current Main mod (unless it also specifies an Edition).
    * The title is suffixed with an Edition in brackets if there's a mod enabled with one specified.
* Makes messages shown by the game and hacks support visual styles (if enabled on the game tab of the [[../Settings.md|launcher's settings]]).
* Makes the game DPI Aware (if enabled on the game tab of the [[../Settings.md|launcher's settings]]).
* Makes the game [show a message on startup](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/NoAudioDeviceMessage.png) if there are no audio devices or the Windows Audio service is not running instead of [crashing](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/NoAudioDeviceCrash.png).
    * This can be opted out of with the `-noaudiodevicecheck` [[../CommandLineArguments.md|command line argument]].
* Makes the game show an [assertion failed dialog](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/MerchNull.png) if the loaded save file has more rewards unlocked than are defined in the rewards file instead of the game crashing.
    * You can use the "Ignore" button to continue the game. Saving the game after doing so will cause the fact that the reward was unlocked to disappear from your save data.
* Makes the game get terminated if it takes more than 1 second to exit.
    * This is to stop the game from hanging in the background indefinitely hogging CPU which sometimes happens in this game. 
    * This will show an assertion failed message if you're using the `-testing` [[../CommandLineArguments.md|command line argument]].
* Makes the game reload car camera data when a car gets loaded (such as when calling it from the phone booth).
    * The game normally loads this data again but throws it away instead of keeping the new data.
    * This can be opted out of through a couple different means:
        * As of version 1.23, you can use the `-noreloadcarcameradata` [[../CommandLineArguments.md|command line argument]].
        * Enabling Debug Test and then enabling its "No Reload Car Camera Data" setting on the "Vehicles" page of its Mod Settings.
* Saves crash dumps when the game crashes (if enabled on the game tab of the [[../Settings.md|launcher's settings]]).
* Terminates the game when it crashes (if enabled on the game tab of the [[../Settings.md|launcher's settings]]).
* Shows a message when the game crashes (if enabled on the game tab of the [[../Settings.md|launcher's settings]]).

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=HackSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `HackSupport.ini` and add the parameters necessary for your mod inside it.

**NOTE:** Despite this hack always being enabled, a mod must explicitly require it to configure it.

```ini
; [Miscellaneous] Section
	; OverrideTexture: Specify a texture name that will be forced for every non-animated shader.
	
[Miscellaneous]
OverrideTexture=Texture.png
```

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Debug Text Mode
This hack registers several debug modes for the [[DebugText.md]] hack when used alongside it.

# Version History
This hack changes in practically every version of the Mod Launcher to accommodate other hacks so only some specific changes are listed here.

## Version 1.25.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/Hacks/HackSupport.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/HackSupport.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/HackSupport.md }}

## Version 1.23.8
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/HackSupport.md }}

## Version 1.23.6
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.6/Hacks/HackSupport.md }}

## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/Hacks/HackSupport.md }}

## Version 1.23.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/HackSupport.md }}

## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/HackSupport.md }}

## Version 1.22.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.4/Hacks/HackSupport.md }}

## Version 1.22.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/HackSupport.md }}

## Version 1.22.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.1/Hacks/HackSupport.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/HackSupport.md }}

## Version 1.17
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/HackSupport.md }}

## Version 1.16
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16/Hacks/HackSupport.md }}

## Version 1.15
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15/Hacks/HackSupport.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/HackSupport.md }}

## Version 1.12
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12/Hacks/HackSupport.md }}