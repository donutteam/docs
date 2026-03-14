---
title: "Custom Bonus Mission Support"
description: "This hack allows mods to control various aspects of bonus missions such as the characters that host them."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 367 # 1.14
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to control various aspects of bonus missions such as the characters that host them.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomBonusMissionSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomBonusMissionSupport.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; StreetRaceIntroDialogueMissionIndex: The dialogue index of the third street race character.
		; Defaults to 11. You probably won't have any reason to ever change this.
	
; [StreetRaceIntroDialogueMissionIndex] Section
	; CHARNAME: Bind a first or second street race character to index 9 or 10 respectively.
		; 9 is the index you would use for the SR1 NPC.
		; 10 is the index you would use for the SR2 NPC.
		; The SR3 NPC does not need to be assigned here.
	
; [StreetRaceIntroDialogueMissionIndexLX] Section
	; CHARNAME: Bind a first or second street race character to index 9 or 10 respectively.
		; 9 is the index you would use for the SR1 NPC.
		; 10 is the index you would use for the SR2 NPC.
		; The SR3 NPC does not need to be assigned here.
	
; [LXSRX] Section,
	; ResetPlayer: Force reset the mission once while initially loading it. 
		; Defaults to 1.
	; ForcePlayerInCar: Force the player in the car at the start of any given mission.
		; Defaults to 1.
	
; [LXMX] Section,
; [LXBM1] Section
	; These parameters can also be used on bonus missions and, contrary to the name of the hack, story missions.
	; The default values, however, are different.

	; ResetPlayer: Force reset the mission once while initially loading it.
		; Defaults to 0.
	; ForcePlayerInCar: Force the player in the car at the start of any given mission.
		; Defaults to 0.

; [StartBitmaps] Section
	; Allows you to set what mission presentation bitmaps are loaded when starting bonus missions or street races, based on the host character.

	; CHARNAME: Set the mission presentation bitmap to use when starting a mission hosted by the specified character in this level.
		; Various base game characters have bitmaps assigned, see below.

; [StartBitmapsLX] Section
	; Allows you to set what mission presentation bitmaps are loaded when starting bonus missions or street races, based on the host character, for a specific level.

	; CHARNAME: Set the mission presentation bitmap to use when starting a mission hosted by the specified character in this level.
		; Defaults to the global start bitmap for the character, if there is one.

; [EndBitmaps] Section
	; Allows you to set what mission presentation bitmaps are loaded at the end of bonus missions or street races with the "Patty & Selma" screen, based on the mission.

	; MISSION_NAME: Set the mission presentation bitmap to use on the "Patty & Selma" screen for the specified mission name on all levels.
		; Valid values include bm1, sr1, sr2, sr3, gr1, etc.
		; Defaults to the Default.

; [EndBitmapsLX] Section
	; Allows you to set what mission presentation bitmaps are loaded at the end of bonus missions or street races with the "Patty & Selma" screen, based on the mission.

	; Default: Set the mission presentation bitmap to use on the "Patty & Selma" screen for this level.
	; MISSION_NAME: Set the mission presentation bitmap to use on the "Patty & Selma" screen for the specified mission name on all levels.
		; Valid values include bm1, sr1, sr2, sr3, gr1, etc.
		; Defaults to the level's default.
	
[Miscellaneous]
StreetRaceIntroDialogueMissionIndex=11

[StreetRaceIntroDialogueMissionIndex]
; Level 1-6 SR1 and SR2 NPCs
milhouse=9
nelson=10

; Level 7 SR1 and SR2 NPCs
zmale3=9
zfem1=10

[L2SR3]
ResetPlayer=1
ForcePlayerInCar=1

[StartBitmaps]
b_nelson=art/frontend/dynaload/images/misXX_CT.p3d
b_milhouse=art/frontend/dynaload/images/misXX_TT.p3d
b_ralph=art/frontend/dynaload/images/misXX_CP.p3d
b_louie=art/frontend/dynaload/images/misXX_GB.p3d
b_witch=art/frontend/dynaload/images/misXX_HW.p3d
b_zfem1=art/frontend/dynaload/images/misXX_HW.p3d
b_zmale1=art/frontend/dynaload/images/misXX_HW.p3d
b_zmale3=art/frontend/dynaload/images/misXX_HW.p3d

b_cletus=art/frontend/dynaload/images/mis01_08.p3d
b_grandpa=art/frontend/dynaload/images/mis02_08.p3d
b_skinner=art/frontend/dynaload/images/mis03_08.p3d
b_cbg=art/frontend/dynaload/images/mis04_08.p3d
b_frink=art/frontend/dynaload/images/mis05_08.p3d
b_snake=art/frontend/dynaload/images/mis06_08.p3d
b_smithers=art/frontend/dynaload/images/mis07_08.p3d

[EndBitmapsL1]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL2]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL3]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL4]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL5]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL6]
Default=art/frontend/dynaload/images/misXX_PS.p3d

[EndBitmapsL7]
Default=art/frontend/dynaload/images/misXX_HW.p3d
```

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomBonusMissionSupport.md }}

## Version 1.17
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomBonusMissionSupport.md }}

## Version 1.15.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15.1/Hacks/CustomBonusMissionSupport.md }}