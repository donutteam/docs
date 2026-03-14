---
title: "Per Level Coin Count"
description: "This hack makes levels have separate coin counts."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack makes levels have separate coin counts.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=PerLevelCoinCount
```

Your mod can provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `PerLevelCoinCount.ini` and add the parameters necessary for your mod inside it.

```ini
[SharedWallet]
; Declare a shared wallet for multiple levels.

; Level
;	Add a level to this shared wallet.
;	Any given level can only be in ONE SharedWallet.
Level=1
Level=7
```