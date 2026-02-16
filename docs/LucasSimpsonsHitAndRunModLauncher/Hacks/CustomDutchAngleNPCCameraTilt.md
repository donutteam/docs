---
title: "Custom Dutch Angle NPC Camera Tilt"
description: "This hack that allows mods to enable the camera tilting near NPCs, like it normally does in vanilla Level 7, in whatever levels they like with a configuration file to customise the angle."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack that allows mods to enable the camera tilting near NPCs, like it normally does in vanilla Level 7, in whatever levels they like with a configuration file to customise the angle.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomDutchAngleNPCCameraTilt
```

# Configuring This Hack
To configure this hack, create a file named `CustomDutchAngleNPCCameraTilt.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>

<!--
<CustomDutchAngleNPCCameraTilt>
	TiltAngle: Specify the angle the camera should tilt at in levels/missions where this is enabled.
		Defaults to ~10 degrees.

	<Level>
		Index: The index of the level (zero-based).
		 OR
		Number: The number of the level (one-based).

		DutchCameraTilt: Whether to enable dutch camera tilt when standing near NPCs in this level.
			Defaults to true for Level 7 and false for all other levels.

		TiltAngle: Specify the angle the camera should tilt at in this level and its missions when this is enabled.
			Defaults to the global TiltAngle.

		<Mission>
			Index: The index of the mission (zero-based).
			 OR
			Number: The number of the mission (one-based).

			DutchCameraTilt: Whether to enable dutch camera tilt when standing near NPCs in this mission.
				Defaults to the Level's DutchCameraTilt.

			TiltAngle: Specify the angle the camera should tilt at in this mission.
				Defaults to the Level's TiltAngle.
-->

<!-- Go full australia when tilting the camera -->
<CustomDutchAngleNPCCameraTilt TiltAngle="180">
	<!-- Enable NPC camera tilting for all of Level 1 -->
    <Level Number="1" DutchCameraTilt="true">
		<!-- Except Mission 1! -->
        <Mission Number="1" DutchCameraTilt="false" />
    </Level>

	<!-- Enable for all of level 2 with a less extreme angle -->
    <Level Number="2" DutchCameraTilt="true" TiltAngle="15" />

	<!-- Disable for Level 7 -->
	<Level Number="7" DutchCameraTilt="false" />
</CustomDutchAngleNPCCameraTilt>
```