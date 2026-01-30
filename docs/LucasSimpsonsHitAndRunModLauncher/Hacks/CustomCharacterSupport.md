---
title: "Custom Character Support"
description: "This hack allows you to enable certain features on new and existing characters."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 376 # 1.17
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows you to enable certain features on new and existing characters.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomCharacterSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomCharacterSupport.ini` and add the parameters necessary for your mod inside it.

```ini
; [CHARNAME] Section: Set values for character specified in place of CHARNAME.
	; BlendModeSupport
		; Allows the usage of Additive and Subtractive shaders on this character. 
		; Defaults to 0, meaning all shaders will be forced to Alpha.
	; IsLisa
		; Forces the character to sit 0.12 meters higher in either seat of a car.
		; Defaults to 1 for any character whose name is "lisa" or starts with "l_".
	; IsMarge
		; Stops joints 33, 34 and 35 of the skeleton (Marge's hair) from getting bent down in a car that has SetHighRoof set to 0.
		; Defaults to 1 for any character whose name is "marge" or starts with "m_".
	; IdleAnimationWeight
		; This can be specified once for each idle animation for this skin in the player character's CHO file to control how common each idle animation.
		; The values are relative to one another.
		; Effectively defaults to 5 for the first one, 3 for the second one and 2 for the first one (50%, 30% and 20% chances respectively).

; Other Notes
	; Any character whose internal name starts with m_ or l_ are considered Marge (IsMarge) or Lisa (IsLisa) respectively by default.

[lisa]
BlendModeSupport=0
IsLisa=1
	
[marge]
BlendModeSupport=0
IsMarge=1

[homer]
; All idle animation weights add up to 10
; So a weight of 5 is effectively a 50% chance
IdleAnimationWeight=5
IdleAnimationWeight=3
IdleAnimationWeight=2
```

# Version History
## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomCharacterSupport.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomCharacterSupport.md }}

## Version 1.17.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.2/Hacks/CustomCharacterSupport.md }}