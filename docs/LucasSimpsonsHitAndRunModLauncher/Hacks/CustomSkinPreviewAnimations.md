---
title: "Custom Skin Preview Animations"
description: "This hack allows mods to control what animation plays when viewing skins in a skin shop."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to control what animation plays when viewing skins in a skin shop.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomSkinPreviewAnimations
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomSkinPreviewAnimations.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; 0 to 6: Animation used for each level.
		; 0 = Level 1
		; 1 = Level 2
		; And so on.

; Notes
	; These are the default animations for the regular game.
	; You should only use animations present in the level character's animations file.
	; This should work with any of a character's animations, though it might look odd if the animation doesn't seamlessly loop.

[Miscellaneous]
0=hom_loco_idle_rest
1=brt_loco_idle_rest
2=lsa_loco_idle_rest
3=mrg_loco_idle_rest
4=apu_loco_idle_rest
5=brt_loco_idle_rest
6=hom_loco_idle_rest
```