---
title: "Frame Rate Counter"
description: "This hack adds a frame rate counter to the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds a frame rate counter to the game.

# Settings
## Method
The method used to count the frames. Possible options are:
* Count Frames Each Second
* Average Frame Interval
* Radical Average Frame Time

**Defaults to Radical Average Frame Time.**

## Update Interval (Seconds)
When **Method** is set to **Average Frame Interval**, this sets how frequently the frame rate counter updates.

**Defaults to 0.5.**

## Decimal Places
The number of decimal places to show on the frame rate counter.

**Defaults to 1.**

## Style
### Position
Controls the location of the frame rate counter. Possible options are:
* Top Left
* Top Right
* Bottom Right
* Bottom Left

**Defaults to Bottom Right.**

### Background
The type of background to render behind the frame rate counter's text. Possible options are:
* None
* Drop Shadow
* Rectangle

**Defaults to Drop Shadow.**

### Foreground Colour
The colour of the frame rate counter's text.

**Defaults to fully opaqure white.**

### Background Colour
The colour of the frame rate counter's background.

**Defaults to fully opaque black.**

### Background Rectangle Opacity.
When **Background** is set to **Rectangle**, this controls the opacity of the rectangle.

**Defaults to 0.5.**

# Notes
This was previously distributed as a standalone test hack for previous versions of the Mod Launcher.