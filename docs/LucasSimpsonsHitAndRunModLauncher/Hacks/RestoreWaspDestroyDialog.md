---
title: "Restore Wasp Destroy Dialog"
description: "This hack makes the game play dialog when destroying wasp cameras, as was seemingly originally intended."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack makes the game play dialog when destroying wasp cameras, as was seemingly originally intended.

When it is enabled, one of the player character's `breakca` lines (if they have any, which all base game player characters **do**) will be played when destroying a wasp camera.

# Settings
## Disable Object Destroy Dialog
Disables the game playing dialog when destroying certain objects, such as the power couplings in Blind Big Brother.

These props use the same collection of voicelines and the dialog can get repetitive.

**Defaults to Disabled.**

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=RestoreWaspDestroyDialog
```

Your mod can provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `RestoreWaspDestroyDialog.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
; DisableObjectDestroyDialog
;	Disables the game playing dialog when destroying certain objects, such as the power couplings in Blind Big Brother.
;	Defaults to 0 OR the user's setting, if they have the hack enabled in the mods list.
DisableObjectDestroyDialog=0
```