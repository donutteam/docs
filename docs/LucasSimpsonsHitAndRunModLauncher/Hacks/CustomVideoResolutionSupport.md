---
title: "Custom Video Resolution Support"
description: "This hack increases the video segment size from 256x256 to a configurable amount."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack increases the video segment size from 256x256 to a configurable amount.

This allows mods to increase the maximum video resolution from about 768x768.
   
These limits do not apply to videos used as textures with [[VideoTextureSupport.md]] as those are instead subject to texture-related limitations.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomVideoResolutionSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomVideoResolutionSupport.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
SegmentWidth=2018
SegmentHeight=1024
```

# Notes
This is the same hack internally as [[IncreasedVideoResolutionSupport.md]].