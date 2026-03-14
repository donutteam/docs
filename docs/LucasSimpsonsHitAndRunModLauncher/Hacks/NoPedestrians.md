---
title: "No Pedestrians"
description: "This hack disables pedestrians."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack disables pedestrians that would typically spawn on loaded [[/Pure3DFiles/ChunkTypes/Path.md]] chunks.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=NoPedestrians
```

# Notes
This was previously part of the [[Multiplayer.md]] hack, but is now a standalone hack it requires.