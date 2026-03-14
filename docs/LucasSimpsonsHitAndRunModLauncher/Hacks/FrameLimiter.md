---
title: Frame Limiter
description: "This hack limits the frame rate of the game to an amount specified in the hack's settings with additional options to configure when and how this is done."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 358 # 1.10
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack limits the frame rate of the game to an amount specified in the hack's settings with additional options to configure when and how this is done.

# Settings
## Target Frame Rate
The frame rate that the hack will attempt to reach with the selected Method (see below for more details).

**Defaults to 60.**

## Limit
### While on Loading Screens
Set whether or not the frame rate will be limited on loading screens. This negatively impacts loading times.

**Defaults to Disabled.**

### While on Menus
Set whether or not the frame rate will be limited on the main menu and the pause menu.

**Defaults to Enabled.**

## Advanced
### Method
The method to use to limit the frame rate. Available options are:
* **Waitable Timer**
* **Sleep**
* **Busy Wait**
* **Sleep and Busy Wait**

**Defaults to Waitable Timer.**

### Compensation Limit (ms)
TODO

**Defaults to 30.**

### High Resolution Timer
Makes the hack use a more precise waitable timer.

**Defaults to Enabled.**

### Load Files While Waiting
This makes it so files can be loaded while the game is waiting for the next frame.

The [[LoadManagerThreadCoordination.md]] hack is used to achieve this.

**Defaults to Disabled.**

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/FrameLimiter.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/FrameLimiter.md }}

## Version 1.23.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/FrameLimiter.md }}

## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/FrameLimiter.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/FrameLimiter.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/FrameLimiter.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/FrameLimiter.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/FrameLimiter.md }}