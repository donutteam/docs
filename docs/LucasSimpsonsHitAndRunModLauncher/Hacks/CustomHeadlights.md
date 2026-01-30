---
title: "Custom Headlights"
description: "This hack allows mods to customise the headlight and taillight brightness for each level of the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to customise the headlight and taillight brightness for each level of the game.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomHeadlights
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomHeadlights.ini` and add the parameters necessary for your mod inside it.

```ini
; [CustomHeadlights] Section: Set Headlight Brightness Per Level
	; 0 to 6: Regular Levels
	; 8 to 14: Bonus Levels
	
; [CustomTailights] Section: Set Tailight Brightness Per Level
	; 0 to 6: Regular Levels
	; 8 to 14: Bonus Levels

[CustomHeadlights]
; Default Headlight Brightness for Main Levels 1-7
0=0
1=0
2=0.2
3=0.6
4=0.4
5=0.4
6=0.6

; Default Headlight Brightness for Bonus Game Levels 1-7
8=1
9=1
10=1
11=1
12=1
13=1
14=1

[CustomTaillights]
; Default Taillight Brightness for Main Levels 1-7
0=0
1=0
2=0.3
3=0.4
4=0.4
5=0.4
6=0.4

; Default Taillight Brightness for Bonus Game Levels 1-7
8=0.4
9=0.4
10=0.4
11=0.4
12=0.4
13=0.4
14=0.4
```