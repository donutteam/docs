---
title: "Walker Camera Data Support"
description: "This hack restores support for the Walker Camera Data chunk in P3D files."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack restores support for the [[/Pure3DFiles/ChunkTypes/WalkerCameraData.md]] chunk in P3D files.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=WalkerCameraDataSupport
```

# Notes
[[/Pure3DFiles/ChunkTypes/WalkerCameraData.md]] was meant to be similar to the [[/Pure3DFiles/ChunkTypes/FollowCameraData.md]] chunk cars have. Supporting dynamic ones via P3D chunks was scrapped, but the camera itself is still used internally.

Due to its scrapped nature, unlike cars that each have their own ID, every character is given an "invalid" ID, which is 9. Because of this, you should call [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/LoadP3DFile.p3d]] on the P3D containing the [[/Pure3DFiles/ChunkTypes/WalkerCameraData.md]] chunk in your `level.mfk`, and the `Index` should always be 9.