---
title: "Sphere Map Reflections"
description: "This hack improves reflections on cars by reimplementing the spheremap PDDI shader type from the console versions of the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 397 # 1.23.4
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

Typically, in the PC version of the game, all `spheremap` shaders are remapped to be `environment` shaders. This hack replaces this remapping with a reimplementation of the `spheremap` PDDI shader type, based on the Xbox version of the game.
 

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/SphereMaps.md }}

## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/Hacks/SphereMaps.md }}