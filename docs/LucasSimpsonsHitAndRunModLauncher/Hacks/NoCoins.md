---
title: "No Coins"
description: "This hack disables coins."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack disables coins.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=NoCoins
```

# Notes
This was previously part of the [[Multiplayer.md]] hack, but is now a standalone hack it requires.