---
title: "Version 1.27"
description: "Changelog for Version 1.27 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

# Launcher
## General
* Made the Mod Launcher itself respect the `-nocarindexmapping` [[../CommandLineArguments.md|command line argument]] during conflict checking.
* Fixed an issue that prevented encrypted mods from loading.
* Updated the Mod Launcher's copyright information.
* Potentially fixed various crashes related to jump lists.
* Improved the dialogue shown when compiling mods to list more details about what was compiled.
* Added a warning on startup if the Mod Launcher detects the game is installed within a cloud directory.
	* This currently attempts to detect Dropbox, Google Drive, OneDrive and iCloud.
	* This can be disabled with the new **Warn on Cloud Directories** setting in Launcher settings.
* Removed `lucasstuff.com` from the list of valid Donut Team URLs.
	* This affects the obscure `-apiurl` and obscure `-updatecheckurl` [[../CommandLineArguments.md]] that pretty much only exist for internal testing.
* Changed the encoding used when reading text files from ANSI to UTF8.
* Made it so, when loading mods, `[PathHandlers]` in `CustomFiles.ini` are validated to ensure that the handler script exists.
* Now checks the digital signature of the [[../Hacks/HackSupport.md]] hack (and therefore, the rest of Hacks.dll) before attempting to launch the game with it.
	* This check helps to ensure it has not been tampered with.
	* If the signature cannot be verified or, if for some inexplicable reason, it is not signed by Donut Team LLC, warning message(s) will be shown.
	* On Windows XP, verifying our signature is not possible and a different message will be shown indicating this.
	* In either case, you can choose to skip the message(s) and run the potentially unsafe code anyways.

## Main Window
* Made it so the **Launch** button is now disabled when the game is attempting to launch and re-enabled when this either succeeds or fails.
* Made it so when Multiplayer is enabled the **Launch** will instead read **Play Multiplayer**.
* Redesigned the main window with a tool strip at the top, containing **File**, **View** and **Help** menus.
	* This tool strip replaces the **Open...** and **Account...** buttons, previously found on the main window, to follow a more universally understood design for programs.
* Fixed a bug where right clicking a mod setting hack that's also requirable by mods and choosing **Copy Require Line** would copy `RequiredMod=HackName` instead of `RequiredHack=HackName`.

## About Window
Added this new window that can be accessed from **Help** > **About...** on the main window's new tool strip.

The **Licenses** tab, previously located on the **Launcher Settings** window, has also now been moved to this new window.

## Mods List
* Added the `-nodeltaupdatemodslist` command line argument to force the Mod Launcher to fully reload the mods list when clicking a reload button.
* Added a new **Multiplayer** tab.
	* This tab is intended to house the Multiplayer hack itself, as well as multiplayer focused mods.
* Added a **Rebindable keys are available in "Mod Settings..."** message to the **About** tab that is shown when customisable keybinds are available for the currently selected mod.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/ModFeatures.md }}

# New Mods
## Analogue Speedometer Resources
Added this new framework that provides resources for the new Analogue Speedometer hack.

This was previously part of the Multiplayer Resources framework.

## Multiplayer Resources
Added this new framework that provides resources for the new Multiplayer hack.

This was previously distributed as part of separate "SHAR MP" builds of the Mod Launcher.

# Removed Mods
## No Audio
Removed this mod. Use the existing No Audio mod hack instead.

## No HUD
Removed this mod. Use the new Developer Keys hack to toggle the HUD instead.

## No Traffic
Removed this mod. Use the new No Traffic mod hack instead.

## Text Names
Removed this mod. Use the new Developer Keys hack to toggle showing text names or enable the Text Names mod hack instead.

## Unlock All Rewards
Removed this mod. The existing Unlock All Outfits, Unlock All Vehicles and Unlock Bonus Game hacks are now mod hacks instead.

# New Hacks
## Additional Quest Reward Types
Added this new hack that adds additional quest reward types.

Currently, this hack only fixes the partially broken existing `cards` reward type so you can add a `car` reward for collecting all cards in a level that works properly.

By default, there is no indicator you unlocked a reward but mods can use the Custom Text hack to tweak the text shown when collecting all cards to convey this.

[[../Hacks/AdditionalQuestRewardTypes.md|Learn More]]

## Ambient Car Support
Added this new advanced hack that provides other hacks the ability to spawn arbitrary cars.

This was previously distributed as part of separate "SHAR MP" builds of the Mod Launcher.

[[../Hacks/AmbientCarSupport.md|Learn More]]

## Analogue Speedometer
Added this new setting hack that adds a fancy analogue speedometer you can toggle with a key.

This is a standalone version of the **Analogue Speedometer** setting that was previously part of the Multiplayer hack.

[[../Hacks/AnalogueSpeedometer.md|Learn More]]

## Custom Collector Card Support
Added this new hack that lets you customise character quote icons, the number of character quotes per card (up to 3), card drawables per card, and card collect drawables per card.

[[../Hacks/CustomCollectorCardSupport.md|Learn More]]

## DearImgui Support
Added this new advanced hack that provides other hacks the ability to render stuff on top of the game using [DearImgui](https://github.com/ocornut/imgui).

[[../Hacks/DearImgui.md|Learn More]]

## Developer Keys
Added this new hack that adds key binds that are useful for mod developers.

This hack was originally called "Map Test Keys" but was renamed to "Developer Keys" per Lord Loren's demand.

[[../Hacks/DeveloperKeys.md|Learn More]]

## Frame Rate Counter
Added this new hack that renders a frame rate counter on top of the game, with various options to configure it.

This was previously distributed as a standalone test hack for previous versions of the Mod Launcher.

[[../Hacks/FrameRateCounter.md|Learn More]]

## Free Camera and No Clip
Added this new hack that allows you to toggle a free camera or no clip mode to move around.

Free Camera hides your character/car and gives you free control of the camera. Upon exiting this mode, you will be returned to where you were restoring what regions were loaded as well as the ped group and traffic group.

No Clip moves your character/car around freely. Upon exiting this mode, they will be dropped wherever you had them.

[[../Hacks/FreeCamera.md|Learn More]]

## Ignore Unsupported DirectInput Devices
A new hack that is always enabled and prevents the game from trying to acquire unsupported DirectInput devices, fixing a black screen on startup caused by certain hardware configurations.

This was previously distributed as the standalone Direct Input Acquire Test hack for previous versions of the Mod Launcher.

[[../Hacks/IgnoreUnsupportedDirectInputDevices.md|Learn More]]

## Multiplayer (Beta)
Added this new hack that is a reworked version of the Multiplayer hack that was previously distributed as part of separate "SHAR MP" builds of the Mod Launcher.

Notably, this new version no longer uses Donut Team accounts in any way and servers can be self hosted by anyone using the new [Project:124].

In addition to this, the following changes were made:
* Changed FreeRoam from being a `RequiredMod` to a `RequiredHack`, making it automatically enabled when Multiplayer is instead of having to enable it separately to launch.
* Removed the `Unreleased` flag, as this hack is now a part of the main Mod Launcher.
* Moved the **Server** tab to the start of the hack's settings.
* Added new **Name** and **Name Colour** settings to control how you appear in game.
* Changed various asserts, indicating stuff has gone at least a little bit wrong, into logs instead.
* Removed the **Analogue Speedometer** setting, as this is now a standalone hack.
* Added the ability to chat with other players directly in the game.
* Removed the **Spectate vehicle while surfing** setting.
	* The camera would not keep up with cars while car surfing without this setting on, so we have elected to make this always enabled.
* Added an in-game safety warning.
	* This is shown briefly on startup to remind players to not share personal information or account credentials with other players.
* Updated this hack to have customizable keybinds.
* Removed the **Play Offline** setting, host a local server instead.
* Removed a hardcoded check to show "Play Level X" instead of "PLAY LEVEL X" main menu items when the Late Night at the Kwik-E-Mart mod is enabled.
	* Sorry, Kenny.
* Removed the `HideFromOnline` attribute from the `<Multiplayer>` element of `Multiplayer.xml`, host a local server instead.
* Made it so players now animate for everyone when getting into a vehicle.
* Added the ability to destroy each other's cars.
	* Husks are not currently supported and are fully disabled.
* No longer requires the No Wrenches hack.
* Now requires the new No Explosion Exit Dely hack.
* Added " (Beta)" to the end of the hack's title to indicate this is still very much a work-in-progress.
* Now requires the Unlock All Outfits hack.
* Now requires the Unlock All Vehicles hack.
* Added the ability for the server to teleport players.
* Reset the **Host** setting and made it now default to `127.0.0.1` instead of `multiplayer.donutteam.com`.
* Removed the `-multiplayerparkedcars` command line argument that enabled parked cars in Multiplayer.
* Now requires the Unlock All Missions hack.

[[../Hacks/Multiplayer.md|Learn More]]

## No Coins
Added this new hack that disables all coins.

This was previously part of the [[../Hacks/Multiplayer.md]] hack, but is now a standalone hack it requires.

[[../Hacks/NoCoins.md|Learn More]]

## No Explosion Exit Delay
Added this new hack that removes the 3 second delay before your characters jumps out of a destroyed car.

[[../Hacks/NoExplosionExitDelay.md|Learn More]]

## No Gags
Added this new hack that disables all gags.

This was previously part of the [[../Hacks/Multiplayer.md]] hack, but is now a standalone hack it requires.

[[../Hacks/NoGags.md|Learn More]]

## No Hit & Runs
Added this new hack that disables Hit & Runs.

This was previously part of the [[../Hacks/Multiplayer.md]] hack, but is now a standalone hack it requires.

[[../Hacks/NoHitAndRuns.md|Learn More]]

## No Pedestrians
Added this new hack that disables all pedestrians.

This was previously part of the [[../Hacks/Multiplayer.md]] hack, but is now a standalone hack it requires.

[[../Hacks/NoPedestrians.md|Learn More]]

## No Traffic
Added this new hack that disables all traffic.

This was previously part of the [[../Hacks/Multiplayer.md]] hack, but is now a standalone hack it requires.

[[../Hacks/NoTraffic.md|Learn More]]

## Restore Wasp Destroy Dialog
Added this new hack that restores dialog for destroying wasp cameras.

[[../Hacks/RestoreWaspDestroyDialog.md|Learn More]]

## Text Names
Added this new hack that makes the game show the internal names of frontend text strings.

It can be enabled the mods list, as well as being toggleable via the new **Developer Keys** and **Trainer** hacks.

[[../Hacks/TextNames.md|Learn More]]

## Trainer
Added this new hack that adds an ingame window for tweaking game parameters on the fly, teleporting around, and more!

[[../Hacks/Trainer.md|Learn More]]

## Walker Camera Data Support
Added this new hack that restores support for the Walker Camera Data chunk in P3D files.

[[../Hacks/WalkerCameraDataSupport.md|Learn More]]

# Updated Hacks
## General
Fixed a crash when activating the Cheat Keys phonebooth when one or more loaded mods had a `CustomShopSupport.xml` containing one or more `<PhoneBooth>` elements containing one or more `<Selector>` elements with a `Locator` attribute.

## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/HackSupport.md }}

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/AdditionalScriptFunctionality.md }}

## Analogue Mouse Input
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/AnalogueMouseInput.md }}

## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/AspectRatioSupport.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/BugFixes.md }}

## Cheat Keys
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CheatKeys.md }}

## Custom Audio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomAudioSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomFiles.md }}

## Custom Interior Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomInteriorSupport.md }}

## Custom Shop Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomShopSupport.md }}

## Custom Trigger Actions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/CustomTriggerActions.md }}

## Debug Test
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/DebugText.md }}

## Unlock All Outfits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/UnlockAllOutfits.md }}

## Unlock All Vehicles
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/UnlockAllVehicles.md }}

## Unlock Bonus Game
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/UnlockBonusGame.md }}