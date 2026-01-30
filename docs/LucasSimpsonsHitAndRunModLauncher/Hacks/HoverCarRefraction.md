---
title: "Hover Car Refraction"
description: "This hack reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 397 # 1.23.4
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game. This reimplementation is based on the Xbox version.

# Settings
## Per Car Screen Capture
This setting makes it so the game will capture the screen before rendering each hover car instead of just when the first one renders. This improves the appearance of multiple hover cars.

**Defaults to Enabled.**

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=HoverCarRefraction
```

When required, this hack will make all the necessary changes to the shaders of `art\\cars\\frink_v.p3d` **unless** the mod requiring it provides it, in which case the mod will be expected to make the changes to the shader on its own.

# Version History
## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/HoverCarRefraction.md }}

## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/Hacks/HoverCarRefraction.md }}