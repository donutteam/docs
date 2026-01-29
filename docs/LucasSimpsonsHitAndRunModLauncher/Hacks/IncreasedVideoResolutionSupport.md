---
title: "Increased Video Resolution Support"
description: "This hack increases the video segment size from 256x256 to 2048x1024."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 361 # 1.11
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByAMod.md }}

This hack increases the video segment size from 256x256 to 2048x1024.

This increases the maximum video resolution from about 768x768 to about 6144x3072.
   
These limits do not apply to videos used as textures with [[VideoTextureSupport.md]] as those are instead subject to texture-related limitations.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=IncreasedVideoResolutionSupport
```

# Version History
## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/IncreasedVideoResolutionSupport.md }}

## Version 1.15.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15.3/Hacks/IncreasedVideoResolutionSupport.md }}