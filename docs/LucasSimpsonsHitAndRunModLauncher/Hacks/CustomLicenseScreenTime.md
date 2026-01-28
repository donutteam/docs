---
title: "Custom License Screen Time"
description: "This hack allows mods to adjust the amount of time spent on the license screen and whether or not the user is able to prematurely skip it."
authors: [ 2 ]
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to adjust the amount of time spent on the license screen and whether or not the user is able to prematurely skip it.

# Requiring This Hack
To require this hack, add this line to the `[Miscellaneous]` section of your mod's Meta.ini:

```ini
RequiredHack=CustomLicenseScreenTime
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomLicenseScreenTime.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
; Time
;	Specify the time, in milliseconds, that the game should remain on the license screen.
;	Use -1 to make the game remain on the license screen until the user skips it.
;	Defaults to 1000.
Time=1000

; Skippable
;	Sets whether the license screen can be skipped with the Enter key.
Skippable=0
```

# Notes
Setting `Time` to `-1` and `Skippable` to 0 makes it impossible to bypass the license screen.

# Version History
## Version 1.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.5/Hacks/CustomLicenseScreenTime.md }}