---
title: "3D Phone Booth Preview Support"
description: "This hack allows mods to have 3D previews in the phone booth in place of the usual 2D sprites."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByAMod.md }}

This hack allows mods to have 3D previews in the phone booth in place of the usual 2D sprites.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=3DPhoneBoothPreviewSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `3DPhoneBoothPreviewSupport.ini` and add the parameters necessary for your mod inside it.

```ini	
[Miscellaneous]
; BackgroundPath
;	The path to the background scene that will be loaded for the 3D Phonebooth.
;   Defaults to art\\frontend\\scrooby\\resource\\pure3d\\rewardbg.p3d.
BackgroundPath=art\\frontend\\scrooby\\resource\\pure3d\\rewardbg.p3d

; DarkenLockedCars
;	Set whether or not locked cars should be dark in color.
;	Defaults to 0.
DarkenLockedCars=0

; FullScreen
;	Set whether or not the scene should be fullscreen.
; 	Defaults to 1.
FullScreen=1

; Radius
;	Set the size of the cars on the pedestal.
; 	Defaults to 3.6.
Radius=3.6
```

# Using This Hack
This hack requires changes to the frontend file `art\frontend\scrooby\ingame.p3d` to function.

**Requiring this hack in a mod without making these changes will cause a crash when opening phone booths.**

The specific changes involve adding the chunks highlighted in the image below to `Phonebooth.pag`.

![frontend changes](/img/LucasSimsponsHitAndRunModLauncher/Hacks/3DPhoneBoothPreviewSupport/FrontendChanges.png)

We distribute a mod called [Project:15] that utilizes this hack and makes these necessary changes. It also re-configures the hack to fit its specific implementation of the feature. If you want to implement this feature into your mod you have a few options:

* Mods that do not modify `art\frontend\scrooby\ingame.p3d` should be compatible with the [Project:15] mod right away.
* Mods that do modify this file can copy the aforementioned chunks into their copy of it and add `SupportedMod=3DPhoneBoothPreviews` to the `[Miscellaneous]` section of their `Meta.ini` to add support for being enabled alongside that mod.
* Mods can force this feature on by copying the chunks, requiring the hack and copying `3DPhoneBoothPreviewSupport.ini` from 3D Phone Booth Previews.

Mods will also need to provide car shop preview models in `art\frontend\dynaload\cars` for any custom cars.

# Version History
## Version 1.18.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.2/Hacks/3DPhoneBoothPreviewSupport.md }}

## Version 1.18.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.1/Hacks/3DPhoneBoothPreviewSupport.md }}