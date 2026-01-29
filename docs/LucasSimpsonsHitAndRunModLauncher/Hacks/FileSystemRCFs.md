---
title: "File System RCFs"
description: "This hack makes the game's RCF files get mounted into the virtual file system, allowing their contents to be accessed by Lua scripts."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 79 # 1.24
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByAMod.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPageHidden.md }}

This hack makes the game's RCF files get mounted into the virtual file system, allowing their contents to be accessed by Lua scripts.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=FileSystemRCFs
```

# Version History
## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/FileSystemRCFs.md }}