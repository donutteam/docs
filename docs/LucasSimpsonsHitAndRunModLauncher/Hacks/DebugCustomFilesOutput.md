---
title: "Debug Custom Files Output"
description: "This hack allows for debugging Custom Files output by writing files output by uncompiled mods to disk."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnDeveloperPage.md }}

This hack allows for debugging Custom Files output by writing files output by uncompiled mods to disk.

When enabled, this hack will write files to `Documents\My Games\Lucas' Simpsons Hit & Run Mod Launcher\Debug Custom Files Output`.

# Settings
## Delete Existing Folder
Delete the existing Debug Custom Files Output folder, if it exists, when starting the game.

**Defaults to Enabled.**

## Replace Existing Files
Replace the existing file, if it exists, when a file is handled.

With this disabled, numbers will be appended to file names to avoid overwriting existing files.

**Defaults to Enabled.**