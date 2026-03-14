---
title: "Analogue Speedometer"
description: "This hack adds a fancy analogue speedometer that can be toggled with a key."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds a fancy analogue speedometer that can be toggled with a key.

# Customization
By default, the image assets for the speedometer are stored in the Mod Launcher's included Analogue Speedometer Resources framework.

This framework contains a single P3D file that the hack loads from `art\\AnalogueSpeedometer.p3d`. This file contains two [[/Pure3DFiles/ChunkTypes/Sprite.md]] chunks:
* Speedometer
* SpeedometerNeedle

You can download a copy of the file here: [AnalogueSpeedometer.p3d](/pure3d/AnalogueSpeedometer.p3d).

A mod can override the file in the framework by placing a custom version of the above file at `CustomFiles/art/AnalogueSpeedometer.p3d` or by adding a Path Handler for `art\\AnalogueSpeedometer.p3d` to modify or redirect it dynamically.

# Settings
## Keybinds
### Toggle Speedometer Visibility
Toggles the visibility of the analogue speedometer.

**Defaults to J.**

# Notes
This is a standalone version of the "Analogue Speedometer" setting that was previously part of the [[Multiplayer.md]] hack.