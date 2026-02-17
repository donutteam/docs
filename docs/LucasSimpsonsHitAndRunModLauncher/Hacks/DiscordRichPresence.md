---
title: "Discord Rich Presence"
description: "This hack adds Discord Rich Presence to the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 375 # 1.16.3
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds Discord Rich Presence to the game.

Main mods are able to extensively customise what is shown on Discord when the player has this hack enabled, if they so choose.

# Configuring This Hack
To configure this hack from a mod when its enabled, create a file named `DiscordRichPresence.ini` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab Version 1.27 }}
These configuration options work starting in Version 1.27.

```ini
[Miscellaneous]
; ApplicationID
; 	Set a custom application ID for your mod.
;	Defaults to our application ID for the Mod Launcher.
ApplicationID="000000000000000000"

[States]
; State strings let you customise what text is shown on Discord during various game states.
; Various variables can be substituted into state strings:
;	$(Level): Shows the LEVEL_X text bible string for the player's current level.
;	$(LevelNumber): Shows the player's current level number.
;	$(BonusGameLevelNumber): Shows the player's current bonus game level number.
;	$(MissionTitle): Shows either:
;		The mission's title set in the relevant section of DiscordRichPresence.ini
;			or if there isn't one
;		The MISSION_TITLE_LX_MXX text bible string for the player's current mission.

; MainMenu
; 	Set what text is shown while the player is on the main menu.
;	Defaults to "Main Menu".
MainMenu="Main Menu"

; BonusGame
; 	Set what text is shown while the player is playing a bonus game level.
;	Defaults to "$(BonusGameLevel) - Bonus Game".
BonusGame="$(BonusGameLevel) - Bonus Game"

; SundayDrive
; 	Set what text is shown while the player is playing a sunday drive mission in a regular game level.
;	Defaults to "$(Level) - Sunday Drive".
SundayDrive="$(Level) - Sunday Drive"

; Mission
; 	Set what text is shown while the player is playing a story mission in a regular game level.
;	Defaults to "$(Level) - $(MissionTitle)".
Mission="$(Level) - $(MissionTitle)"

; BonusMission
; 	Set what text is shown while the player is playing a bonus mission in a regular game level.
;	Defaults to "$(Level) - $(MissionTitle)".
BonusMission="$(Level) - $(MissionTitle)"

; StreetRace
; 	Set what text is shown while the player is playing a street race in a regular game level.
;	Defaults to "$(Level) - $(MissionTitle)".
StreetRace="$(Level) - $(MissionTitle)"

; WagerRace
; 	Set what text is shown while the player is playing a wager race in a regular game level.
;	Defaults to "$(Level) - $(MissionTitle)"
WagerRace="$(Level) - $(MissionTitle)"

; Unknown
; 	Set what text is shown while the game is in an unknown state.
;	Defaults to "In Game".
Unknown="In Game"

[LXMYSD]
; Sunday Drive Specific Stuff
;	Substitute X for a level number from 1 to 7.
;	Substitute Y for a mission number from 0 to 10.

; Title
;	Override the mission's title for rich presence.
Title="Not The Text Bible String"

; LargeImage
;	Override the LargeImage shown during this mission.
LargeImage="some_art_asset_in_discord_dev_portal"

; LargeImageText
;	Override the text shown when hovering over the LargeImage during this mission.
LargeImageText="Some fun flavor text about the mission?"

[LXMY]
; Mission Specific Stuff
;	Substitute X for a level number from 1 to 7.
;	Substitute Y for a mission number from 0 to 10.
;	(has the same properties as the [LXMYSD] section)

[LXBM1]
; Bonus Mission Specific Stuff
;	Substitute X for a level number from 1 to 7.
;	(has the same properties as the [LXMYSD] section)

[LXSRY]
; Street Race Specific Stuff
;	Substitute X for a level number from 1 to 7.
;	Substitute Y for a mission number from 1 to 3.
;	(has the same properties as the [LXMYSD] section)

[LXGR1]
; Wager Race Specific Stuff
;	Substitute X for a level number from 1 to 7.
;	(has the same properties as the [LXMYSD] section)
```
{{ endtab }}
{{ tab Previous Versions }}
These configuration options only work prior to Version 1.27.

```ini
; [Global] Section: Set the titles for missions on every level.
    ; Currently only supports setting the titles for the Bonus Missions, Street Races and Wager Races.

[Global]
BonusMission="Example Bonus Mission"
StreetRace1="Example Street Race 1"
StreetRace2="Example Street Race 2"
StreetRace3="Example Street Race 3"
WagerRace="Example Wager Race"
```
{{ endtab }}
{{ endtabs }}

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/DiscordRichPresence.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/DiscordRichPresence.md }}

## Version 1.23.8
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/DiscordRichPresence.md }}

## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/DiscordRichPresence.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DiscordRichPresence.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/DiscordRichPresence.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DiscordRichPresence.md }}