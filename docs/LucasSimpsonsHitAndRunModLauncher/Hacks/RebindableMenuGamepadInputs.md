---
title: "Rebindable Menu Gamepad Inputs"
description: "This hack allows you to rebind the controller inputs used for the Accept and Back actions in menus. It also allows you to optionally pause the game with the Back button(s)."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 402 # 1.23.9
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack allows you to rebind the controller inputs used for the Accept and Back actions in menus. 

It also allows you to optionally pause the game with the Back button(s).

# Settings
## Accept Input
### Primary
Sets the primary button used for the Accept input.

**Defaults to Button 0/A.**

### Secondary
Sets the secondary button used for the Accept input.

**Defaults to -.**

## Back Input
### Primary
Sets the primary button used for the Back input.

**Defaults to Button 1/B.**

### Pause with Primary
Allows you to pause the game with the primary Back input.

**Defaults to Disabled.**

### Secondary
Sets the secondary button used for the Back input.

**Defaults to -.**

### Pause with Secondary
Allows you to pause the game with the secondary Back input.

**Defaults to Enabled.**

## Function 1 (F1) Input
### Primary
Set the primary button used for the Function 1 (F1) input.

**Defaults to -.**

### Secondary
Set the secondary button used for the Function 1 (F1) input.

**Defaults to -.**

## Function 2 (F1) Input
### Primary
Set the primary button used for the Function 2 (F2) input.

**Defaults to -.**

### Secondary
Set the secondary button used for the Function 2 (F2) input.

**Defaults to -.**

# Notes
* Setting **Back Input > Secondary** to **Button 7/Start** allows you to pause with the start button, like the console versions of the game.
* Setting **Function 1 (F1) Input > Primary/Secondary** or **Function 2 (F2) Input > Primary/Secondary** allows you to enter cheat codes with a gamepad, similar to the console versions of the game.
	* Unlike the console versions, however, holding both inputs is not required to enter cheats.

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/RebindableMenuGamepadInputs.md }}