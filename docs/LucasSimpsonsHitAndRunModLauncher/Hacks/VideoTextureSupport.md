---
title: "Video Texture Support"
description: "This hack allows you to use Bink video files as textures."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows you to use Bink video files as textures.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=VideoTextureSupport
```

# Using This Hack
Bink video files intended for use with this hack have the same restrictions that normal textures do. That is to say, they must be powers of 2 on the width and height (32x32, 64x128, 256x512, etc.).

To add a video texture to your P3D file using [[/LucasPure3DEditor/Intro.md|Lucas' Pure3D Editor]], you just need to modify the "Texture" parameter of a [[/Pure3DFiles/ChunkTypes/Shader.md]]. The value has to be a path starting with a `/` inside the [[CustomFiles/Intro.md|Custom Files]] [[CustomFiles/VirtualFileSystem.md]].

It is recommended that you use `/GameData/` though other paths within the virtual file system will also work.

![video texture example path](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/VideoTextureSupport/Pure3DEditorExample.png)

If the movie has transparency, it's also important to set the "Blend Mode" to "Alpha". Other Blend Modes are also supported.

# Debug Text Mode
This hack registers a debug mode for the [[DebugText.md]] hack when used alongside it.