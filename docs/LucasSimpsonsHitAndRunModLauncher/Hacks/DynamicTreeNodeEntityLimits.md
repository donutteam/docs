---
title: "Dynamic Tree Node Entity Limits"
description: "This hack makes it so tree node entity limits get increased when their lists become full instead of corrupting the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPageHidden.md }}

This hack makes it so [[/Pure3DFiles/ChunkTypes/TreeNode.md]] limits get increased when their lists become full instead of corrupting the game.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=DynamicTreeNodeEntityLimits
```

# Version History
## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/DynamicTreeNodeEntityLimits.md }}