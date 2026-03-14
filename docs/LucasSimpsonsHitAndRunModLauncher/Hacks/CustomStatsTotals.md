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

This hack allows mods to extensively customise how many levels there are in the game and the stats totals for each one.

Some totals are adjusted automatically, while others can be manually configured.

Under certain circumstances, various menus in the game's scrapbook are also disabled to avoid crashing the game.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomStatsTotals
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomStatsTotals.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
; Levels
;	Set the the maximum amount of levels, up to 7.
;	Defaults to 7.
Levels=7

; RemoveUnusedMissionFromMissionSelect
;	Whether to remove unused story mission slots from the Mission Select menu.
;	Defaults to 1.
RemoveUnusedMissionFromMissionSelect=1

[LevelX]
; Customise the totals for a specific level.
;	Substitute X for a level number from 1 to 7.

; StoryMissions
;	Set the number of story missions in the level from 0 to 7.
;	Setting this to 0 prevents mission selecting to the level.
;	That might make sense for a single level mod with no story missions, though.
;	Defaults to 7.
StoryMissions=7

; BonusMissions
;	Set the number of bonus missions in the level from 0 to 1.
;	Defaults to 1.
BonusMissions=1

; StreetRaces
;	Set the number of street races in the level from 0 to 3.
;	Defaults to 3.
StreetRaces=3

; CollectorCards
;	Set the number of collector cards in the level from 0 to 7.
;	Defaults to 7.
CollectorCards=7

; Movies
;	Set the number of movies in the level from 0 to 1.
;	Defaults to 1.
Movies=1

; IncludeMovieInTotal
;	Whether to include this level's movie in the scrapbook's Game Total.
;	Defaults to 1 for Level 3 and 0 for all other levels.
;	Forced to 0 if Movies is set to 0 for the level.
IncludeMovieInTotal=0
```

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomStatsTotals.md }}

## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomStatsTotals.md }}

## Version 1.16
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16/Hacks/CustomStatsTotals.md }}