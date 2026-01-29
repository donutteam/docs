---
title: "FLAC Support"
description: "This hack adds support for using FLAC files in place of RSD files."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByAMod.md }}

This hack adds support for using FLAC files in place of RSD files.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=FLACSupport
```

# Using This Hack
Require the hack and use FLAC files instead of RSD files.

Note that you still need to use the same sample rate and the correct amount of channels.

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/FLACSupport.md }}