---
title: "Custom Stats Totals"
description: "This hack adjusts car and skin reward totals for each level based on the amount defined in the rewards file."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 350 # 1.6
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack adjusts car and skin reward totals for each level based on the amount defined in the rewards file. It also automatically disables scrap book menus for specific levels if there's too many cars or skins to avoid crashing the game.

It also allows mods to specify the maximum amount of Levels the mod has.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomStatsTotals
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomStatsTotals.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous]
	; Levels: The maximum amount of levels.
		; Defaults to 7.

[Miscellaneous]
Levels=7
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomStatsTotals.md }}

## Version 1.16
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16/Hacks/CustomStatsTotals.md }}