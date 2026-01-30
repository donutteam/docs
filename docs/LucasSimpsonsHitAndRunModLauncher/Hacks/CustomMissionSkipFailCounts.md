---
title: "Custom Mission Skip Fail Counts"
description: "This hack allows mods to customise the amount of failures required for the Skip option to display on the mission failed screen."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 347 # 1.5
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to customise the amount of failures required for the Skip option to display on the mission failed screen.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomMissionSkipFailCounts
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomMissionSkipFailCounts.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; FailCount: Global Fail Count for every mission. 
		; Defaults to 7.
	; FailCountLX: Level Specific Fail Count. 
		; Defaults to FailCount.
	; FailCountLXMX: Mission Specific Fail Count. 
		; Defaults to FailCountLX.

; Notes
	; Use -1 for any of these values to prevent skipping.
	; FailCount and FailCountLX do not affect L7M5, L7M6, and L7M7. These missions default to -1 and you must explicitly set each one using FailCountLXMX to change this.

[Miscellaneous]
FailCountL1=4
FailCountL1M5=1
```