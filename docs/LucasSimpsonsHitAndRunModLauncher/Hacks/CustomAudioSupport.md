---
title: "Custom Audio Support"
description: "This hack allows mods to control various audio related features such as the starting ambience track for each story mission."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to control various audio related features such as the starting ambience track for each story mission.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomAudioSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomAudioSupport.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>
<CustomAudioSupport MusicSamplingRate="24000">
	<!--

	<CustomAudioSupport>
		ForcedMusicRMSLevel: Specify an RMS file to load at startup and use all the time. 
			This will prevent the game from ever unloading that level's RMS file.
			This means this can be used for seamless music when switching to/from the main menu and between levels.
		MusicSamplingRate: Defaults to 24,000. Optional.
				
	<Interior>
		Name: The name of the interior.
		MusicEventIndex: The index of the music event to trigger when entering the interior.
		
	<Level>
		Index: The index of the level (zero-based).
		OR
		Number: The number of the level (one-based).
		
		StartAmbienceEventIndex: The ambience index that will be used for mission's that use 76 (interior).
		<Mission>
			Index: The index of the mission from 0 to 7.
				0 refers to the Tutorial in Level 1.
				0 refers to Mission 1 in Levels 2 to 7.
				7 does nothing in Levels 2 to 7 since there is only the 7 story missions and no tutorial.
			StartAmbienceEventIndex: The ambience index that will be used when selecting the mission.
				76 means the mission starts in an interior and it will use the one specified on the level.
		
	-->

	<Interior Name="KwikEMart" MusicEventIndex="20"/>
	<Interior Name="SpringfieldElementary" MusicEventIndex="21"/>
	<Interior Name="SimpsonsHouse" MusicEventIndex="19"/>
	<Interior Name="Krustylu" MusicEventIndex="19"/>
	<Interior Name="dmv" MusicEventIndex="23"/>
	
	<Level Number="1" StartAmbienceEventIndex="9">
		<Mission Index="0" StartAmbienceEventIndex="6" />
		<Mission Index="1" StartAmbienceEventIndex="6" />
		<Mission Index="2" StartAmbienceEventIndex="6" />
		<Mission Index="3" StartAmbienceEventIndex="6" />
		<Mission Index="4" StartAmbienceEventIndex="39" />
		<Mission Index="5" StartAmbienceEventIndex="6" />
		<Mission Index="6" StartAmbienceEventIndex="6" />
		<Mission Index="7" StartAmbienceEventIndex="26" />
	</Level>
	<Level Number="2" StartAmbienceEventIndex="7">
		<Mission Index="0" StartAmbienceEventIndex="4" />
		<Mission Index="1" StartAmbienceEventIndex="4" />
		<Mission Index="2" StartAmbienceEventIndex="4" />
		<Mission Index="3" StartAmbienceEventIndex="4" />
		<Mission Index="4" StartAmbienceEventIndex="4" />
		<Mission Index="5" StartAmbienceEventIndex="4" />
		<Mission Index="6" StartAmbienceEventIndex="4" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
	<Level Number="3" StartAmbienceEventIndex="25">
		<Mission Index="0" StartAmbienceEventIndex="22" />
		<Mission Index="1" StartAmbienceEventIndex="22" />
		<Mission Index="2" StartAmbienceEventIndex="22" />
		<Mission Index="3" StartAmbienceEventIndex="29" />
		<Mission Index="4" StartAmbienceEventIndex="22" />
		<Mission Index="5" StartAmbienceEventIndex="24" />
		<Mission Index="6" StartAmbienceEventIndex="24" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
	<Level Number="4" StartAmbienceEventIndex="51">
		<Mission Index="0" StartAmbienceEventIndex="76" />
		<Mission Index="1" StartAmbienceEventIndex="47" />
		<Mission Index="2" StartAmbienceEventIndex="48" />
		<Mission Index="3" StartAmbienceEventIndex="48" />
		<Mission Index="4" StartAmbienceEventIndex="48" />
		<Mission Index="5" StartAmbienceEventIndex="48" />
		<Mission Index="6" StartAmbienceEventIndex="48" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
	<Level Number="5" StartAmbienceEventIndex="7">
		<Mission Index="0" StartAmbienceEventIndex="4" />
		<Mission Index="1" StartAmbienceEventIndex="4" />
		<Mission Index="2" StartAmbienceEventIndex="4" />
		<Mission Index="3" StartAmbienceEventIndex="4" />
		<Mission Index="4" StartAmbienceEventIndex="4" />
		<Mission Index="5" StartAmbienceEventIndex="4" />
		<Mission Index="6" StartAmbienceEventIndex="4" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
	<Level Number="6" StartAmbienceEventIndex="70">
		<Mission Index="0" StartAmbienceEventIndex="67" />
		<Mission Index="1" StartAmbienceEventIndex="67" />
		<Mission Index="2" StartAmbienceEventIndex="64" />
		<Mission Index="3" StartAmbienceEventIndex="47" />
		<Mission Index="4" StartAmbienceEventIndex="64" />
		<Mission Index="5" StartAmbienceEventIndex="67" />
		<Mission Index="6" StartAmbienceEventIndex="67" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
	<Level Number="7" StartAmbienceEventIndex="53">
		<Mission Index="0" StartAmbienceEventIndex="76" />
		<Mission Index="1" StartAmbienceEventIndex="57" />
		<Mission Index="2" StartAmbienceEventIndex="50" />
		<Mission Index="3" StartAmbienceEventIndex="76" />
		<Mission Index="4" StartAmbienceEventIndex="76" />
		<Mission Index="5" StartAmbienceEventIndex="57" />
		<Mission Index="6" StartAmbienceEventIndex="57" />
		<Mission Index="7" StartAmbienceEventIndex="76" />
	</Level>
</CustomAudioSupport>
```

# Debug Text Mode
This hack registers a debug mode for the [[DebugText.md]] hack when used alongside it.

# Version History
## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomAudioSupport.md }}