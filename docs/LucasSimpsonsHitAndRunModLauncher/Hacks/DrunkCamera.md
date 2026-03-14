---
title: "Drunk Camera"
description: "This hack that makes the camera wobble side to side, as though you are drunk. Probably fun for challenge runs or if you enjoy motion sickness!"
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeRequiredByMod.md }}

This hack that makes the camera wobble side to side, as though you are drunk. Probably fun for challenge runs or if you enjoy motion sickness!

# Settings
## Min Degrees
The minimum angle of the camera.

**Defaults to -10.0.**

## Max Degrees
The maximum angle of the camera.

**Defaults to 10.0.**

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=DrunkCamera
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `DrunkCamera.ini` and add the parameters necessary for your mod inside it.

```ini
[CameraSettings]
; MinDegrees
;	Set the minimum angle of the camera.
;	Optional, defaults to -10.0 OR the user's setting, if they have the hack enabled on the Settings page.
MinDegrees=-10.0

; MaxDegrees
;	Set the maximum angle of the camera.
;	Optional, defaults to 10.0 OR the user's setting, if they have the hack enabled on the Settings page.
MaxDegrees=10.0
```

# Notes
This hack is the result of a dumb joke made while we were working on [[CustomDutchAngleNPCCameraTilt.md]].