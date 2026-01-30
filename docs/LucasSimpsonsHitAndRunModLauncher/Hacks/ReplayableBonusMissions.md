---
title: "Replayable Bonus Missions"
description: "This hack allows bonus missions to be played more than once."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 362 # 1.12
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack allows bonus missions to be played more than once.

By default, the game will require the level to be fully reloaded in order to play it again but mods can change the arguments given to [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/AddNPCCharacterBonusMission.md]] to make it replayable immediately.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=ReplayableBonusMissions
```

# Version History
## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/ReplayableBonusMissions.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/ReplayableBonusMissions.md }}