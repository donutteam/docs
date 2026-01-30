---
title: "Increased Reward Limits"
description: "This hack increases some reward related limits when it's required as well as being configurable for some more advanced limits."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 376 # 1.17
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack increases some reward related limits when it's required as well as being configurable for some more advanced limits.

# Limits
This table indicates what reward related limits exist in the original game and what they're increased to with this hack.

| Limit                                                 | Original Limit | Increased Limit              |
|-------------------------------------------------------|----------------|------------------------------|
| Maximum "forsale" Rewards Per Level in the Saved Game | 12             | Infinite                     |
| Maximum "forsale" Rewards Per Level                   | 8              | Infinite                     |
| Maximum Skins in Skin Shops                           | 4              | Defaults to 64, Configurable |
| Maximum Cars in the Phonebooth and Car Shops          | 64             | Defaults to 64, Configurable |
| Maximum Car Health Values in Save Data                | 60             | Not Increased                |
| Maximum Car Attributes                                | 50             | Infinite                     |

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=IncreasedRewardLimits
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `IncreasedRewardLimits.ini` and add the parameters necessary for your mod inside it.

```ini
; IncreasedRewardLimits.ini
	; Increase some more advanced limits that must be set to an exact number.
	
; [Previews] Section

[Previews]
; CarLimit
;	The maximum amount of cars that can be in skin shop or a phonebooth. 
;	Defaults to 64.
CarLimit=64

; SkinLimit:
;	The maximum amount of skins that can be in skin shops. 
; 	Defaults to 64 with this hack enabled and 4 without it.
; 		(This is because the hack used to simply increase this limit to 64 by default.)
SkinLimit=64
```

# Version History
## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/IncreasedRewardLimits.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/IncreasedRewardLimits.md }}