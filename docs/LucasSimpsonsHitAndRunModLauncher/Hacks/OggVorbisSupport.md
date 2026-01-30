---
title: "Ogg Vorbis Support"
description: "This hack adds support for using Ogg Vorbis files in place of RSD files."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack adds support for using Ogg Vorbis files in place of RSD files.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=OggVorbisSupport
```

# Using This Hack
Require the hack and use OGG files instead of RSD files.

Note that you still need to use the same sample rate and the correct amount of channels.