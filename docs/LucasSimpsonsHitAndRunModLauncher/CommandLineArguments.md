---
title: "Command Line Arguments"
description: "This page documents all the command line arguments for the Mod Launcher."
---

This page documents all the command line arguments for the Mod Launcher.

# CommandLine.txt
As of Version 1.18, the Mod Launcher also supports reading command line arguments out of a file named "CommandLine.txt" placed next to its executable.

In this file, each argument and its parameters must be on a separate line. Parameters also should not have quotes around them where they normally would. The following is an example:

```text
-watermarkopacity
1.0
-testing
-font
Comic Sans MS
20
```

# General
## -crashes
**Added in an unknown version.**

Makes the Mod Launcher save crash dumps at the specified path instead of in your Documents folder.

```text
-crashes "C:\Path\Here"
```

## -currentdirectory
**Added in Version 1.23.10.**

Specify a custom working directory for the Mod Launcher.

```text
-currentdirectory "C:\path\here"
```

## -launchersettings
**Added in Version 1.18.**

Launches the Mod Launcher directly into Launcher Settings.

```text
-launchersettings
```

## -nocommandlinefile
**Added in Version 1.20.**

Prevents the Mod Launcher from loading command line arguments out of `CommandLine.txt`.

```text
-nocommandlinefile
```

## -nocheckmodchanges
**Added in Version 1.21.**

Makes it so the Mod Launcher does not keep track of Meta.ini files changing.

```text
-nocheckmodchanges
```

## -nodeleteold
**Added in Version 1.20.**

Prevents the Mod Launcher from deleting hacks for old versions of the Mod Launcher. Instead it will show an error when trying to load the hack and ignore it.

This was broken in Version 1.21 but works again as of Version 1.22.

```text
-nodeleteold
```

## -nohacksupportcheck
**Added in Version 1.22.4.**

Disables a check where the Mod Launcher will check if Hack Support is loaded and show an error message if it isn't after starting.

```text
-nohacksupportcheck
```

## -nomodenablewarnings
**Added in Version 1.26.**

Disables warnings shown when mods that specify one are ticked in the Mods List.

```text
-nomodenablewarnings
```

## -nounhandledexceptionhandler
**Added in Version 1.18.**

Disables the Mod Launcher showing a message box for otherwise unhandled exceptions. Instead it will crash in the usual manner programs do.

```text
-nounhandledexceptionhandler
```

## -nosettings
**Added in Version 1.18.**
	
Makes it so the Mod Launcher does not load your settings and does not save any settings.

Any settings changed while using this will be persist for the current session and be thrown away when you close the launcher.

```text
-nosettings
```

## -settingsloadhacks
**Added in Version 1.23.7.**

Makes it so the Launcher Settings window will load all the hacks again like how it used to do prior to this version.

```text
-settingsloadhacks
```

## -testing
**Added in Version 1.18.2.**

Enables some internal testing features of the Mod Launcher such as more strict assert messages.

As of Version 1.19, there is now an [[Hacks/CustomFiles/LuaFunctions/IsTesting.md]] CustomFiles Lua Function that returns true when this is enabled.

As of Version 1.22, this now shows an assert if the game is terminated but takes more than 1 second to exit. This version also adds a "Force Update Pinned Shortcuts" option to the "Open.." menu on the main window to update any pinned shortcuts to contain the Mod Launcher's [App ID](https://docs.microsoft.com/en-us/windows/desktop/shell/appids). This version also makes the "Hacks" category available on the "Settings" and "Developer" pages.

```text
-testing
```

# .NET 3.5 Check
## -nodotnetcheck
**Added in Version 1.18.**

Disables the Mod Launcher checking if you have .NET 3.5 installed.

```text
-nodotnetcheck
```

## -spoofdotnetcheck
**Added in Version 1.21.**

This forces the Mod Launcher to show its message box about .NET 3.5 being required.

```text
-spoofdotnetcheck
```

# Account Integration
## -account
**Added in Version 1.22.3.**

Makes the Mod Launcher open directly into the account window.

```text
-account
```

## -accountwindowtoken 
**Added in Version 1.22.**

Re-enables the "token" field on the "Account..." window that was removed in 1.22.

```text
-accountwindowtoken
```

## -apiurl
**Added in Version 1.18.**

Specify a custom Donut Team URL to use for Donut Team Account Integration. 

Must be on `donutteam.com`, `localhost` or a subdomain of those domains. Prior to Version 1.27, `lucasstuff.com` was also supported.

```text
-apiurl "https://api.donutteam.com/"
```

## -commsoptoutdeauthenticate
**Added in Version 1.22.**

This makes the "Deauthenticate" button on the Account window fully remove your account from both the main Mod Launcher and SHAR MP.

```text
-commsoptoutdeauthenticate
```

## -nodtcomms
**Added in Version 1.23.**

Disables Donut Team Account Integration regardless of your setting in the Launcher Settings.

```text
-nodtcomms
```

# App ID
## -appid
**Added in Version 1.22.**
	
This can be used to set a custom App ID for the Mod Launcher.

The App ID defaults to `LucasSimpsonsHitAndRunModLauncher`.

This also disables the updating of Jump Lists.

```text
-appid "LucasSimpsonsHitAndRunModLauncher"
```

## -noappid
**Added in Version 1.22.**

Makes it to the Mod Launcher does not specify an [App ID](https://docs.microsoft.com/en-us/windows/desktop/shell/appids).

This also disables the updating of Jump Lists as they work considerably better with an ID (as they're not bound to the path the program is located at).

```text
-noappid
```

# Appearance
## -font
**Added in Version 1.21.**

Set a custom font for the entire Mod Launcher to use.

```text
-font "Comic Sans MS" 20
```

## -fontscale
**Added in Version 1.18, accidentally removed in Version 1.19 and re-added in 1.21.**

Set the scale of fonts.

Defaults to 1.

```text
-fontscale 1
```

## -lowercasetext
**Added in Version 1.23.**

Makes all the localisable text in the Mod Launcher and messages it shows lowercase.

```text
-lowercasetext
```

## -nowatermark
**Added in Version 1.20.**

Disables the watermark in the Mods list.

```text
-nowatermark
```

## -uppercasetext
**Added in Version 1.23.**

Makes all the localisable text in the Mod Launcher and messages it shows uppercase.

```text
-uppercasetext
```

## -watermarkopacity
**Added in Version 1.22.**

Lets you set the opacity of the watermark in the Mods List.

Defaults to 0.24, can be anywhere from 0 to 1.

```text
-watermarkopacity 0.24
```

# Configurations
## -configuration
**Added in Version 1.21.**

Launch the Mod Launcher with a specific configuration if it exists.

```text
-configuration "DM4 Debug"
```

## -noconfiguration
**Added in Version 1.22.**

Makes the Mod Launcher start on the Main configuration.

```text
-noconfiguration
```

## -notitleconfiguration
**Added in Version 1.21.**

Makes it so the title of the current configuration is not added to the title of the window.

```text
-notitleconfiguration
```
 
# Conflict Checking
## -allowignoremodconflicts
**Added in Version 1.18.**

Allows you to ignore mod conflicts when enabling mods.

As of Version 1.20, this also allows you to bypass conflicts detected when launching the game.

As of Version 1.22.4, this also allows you to skip the error message the Mod Launcher shows when you're using the minimum install of the game.

```text
-allowignoremodconflicts
```

## -ignorelaunchmodconflicts
**Added in Version 1.20.**

Makes the Mod Launcher ignore any conflicts between mods detected when launching the game.

```text
-ignorelaunchmodconflicts
```

## -noscanmodfiles
**Added in Version 1.17.**

Makes the Mod Launcher skip scanning mod files when loading mods. This drastically reduces the loading time of the Mod Launcher *however* modified dates and conflict checking between files in the CustomFiles folders of non-compiled mods will not work. The size of any such mods will also be unavailable in the Advanced tab of the mod's information. The "Show Newest File" option in the right click menu of the mod in the mods list will also not work properly.

```text
-noscanmodfiles
```

## -scanallmodfiles
**Added in Version 1.18.**

Makes the Mod Launcher scan all mod files regardless of whether or not they will compile in. This will cause the mod's modified date to potentially appear differently as well as causing its size to appear larger than it would otherwise. The "Show Newest File" option in the right click menu of the mod in the mods list may also show a different file than it would otherwise.

This was the default behaviour prior to Version 1.18.

```text
-scanallmodfiles
```

# Enabled Mods & Hacks
## -allowedmod
**Added in an unknown version.**

Specify a mod name that will bypass `-ignoreenabledmods`, instead respecting whether or not the user had it enabled.

```text
-allowedmod "Donut Mod 4 Beta"
```

**NOTE**: You must use the name of a mod's folder or LMLM file, not its `InternalName`.

## -enabledmod
**Added in an unknown version.**

Enables the specified mod if it's available.

```text
-enabledmod "Donut Mod 4 Beta"
```

**NOTE**: You must use the name of a mod's folder or LMLM file, not its `InternalName`.

## -ignoreenabledmods
**Added in an unknown version.**

Makes the Mod Launcher ignore any mods or mod hacks the user has enabled, only respecting those enabled with `-enabledmod` or those that bypass this with `-allowedmod`.

```text
-ignoreenabledmods
```

# Filesystem
## -legacyfilesystem
**Added in Version 1.22.**
	
Makes the Mod Launcher use its old virtual file system instead of the new one added in Version 1.22.

```text
-legacyfilesystem
```

## -nofilesystem
**Added in Version 1.22.**

Fully disables the Mod Launcher's virtual filesystem making it basically unusable as far as launching the game goes.

```text
-nofilesystem
```

# Game Launch
## -debuglaunch
**Added in Version 1.18.3.**

Makes the Mod Launcher show a detailed message containing information about how it's going to launch the game when clicking Launch.

As of Version 1.23.2, this message will no longer show up a second time if mods or hacks change in such a way that the Mod Launcher reloads all mods and hacks before starting the game.

```text
-debuglaunch
```

## -launch
**Added in Version 1.10.**

Launches the game with the Mod Launcher with any mods you last had enabled (unless other arguments such as `-ignoremods` disable them).

```text
-launch
```

## -wait
**Added in an unknown version.**

Makes the Mod Launcher stay running in the background when using `-launch` until the game exits.

```text
-wait
```

# Game Window
## -noedition
**Added in Version 1.22.**

Disables the `Edition` feature of Mods and makes it so main mods that specify one show their title like normal main mods would.

```text
-noedition
```

## -nogamemodicon
**Added in Version 1.22.**

Makes it to the game window will not use the icon of the current Main Mod or Edition.

```text
-nogamemodicon
```

# Loading Mods & Hacks
## -allowpartialload
**Added in Version 1.18.**

Makes the cancel button on the loading window cancel loading halfway through keeping anything that was already loaded instead of closing the Mod Launcher.

```text
-allowpartialload
```

## -disablehack
**Added in Version 1.21.**

Disable a specific hack with its InternalName. 

This can be used to forcefully disable hacks that are always enabled.

```text
-disablehack "ModernComputerSupport"
```

## -hack
**Added in an unknown version.**

Makes the Mod Launcher load the hack at the specified path.

```text
-hack "C:\Path\Here\Hack.lmlh"
```

## -hacks
**Added in an unknown version.**

Makes the Mod Launcher load hacks out of the specified path.

```text
-hacks "C:\Path\Here"
```

## -ignorehacks
**Added in an unknown version.**

Makes the Mod Launcher ignore any hacks, only acknowledging those added with `-hack` or `-hacks`.

```text
-ignorehacks
```

## -ignoreloaderrors
**Added in Version 1.23.4.**

Makes the Mod Launcher ignore errors when loading mods and hacks.

```text
-ignoreloaderrors
```

## -ignoremods
**Added in an unknown version.**

Makes the Mod Launcher ignore any mods, only acknowledging those added with `-mod` or `-mods`.

```text
-ignoremods
```

## -ignorerequiredlauncher
**Added in Version 1.18.**

Allows mods and hacks that require a newer version of the Mod Launcher to be loaded and enabled.

```text
-ignorerequiredlauncher
```

## -ignorerequiredsystem
**Added in Version 1.21.**

Allows hacks that do not support the host operating system to be loaded and enabled.

```text
-ignorerequiredsystem
```

## -loadonmainthread
**Added in Version 1.18.**

Makes the Mod Launcher load mods and hacks on the main thread instead of a background thread.

This was the default behaviour prior to Version 1.18.

```text
-loadonmainthread
```

## -mod
**Added in an unknown version.**

Makes the Mod Launcher load the mod at the specified path.

```text
-mod "C:\Path\Here"
```
```text
-mod "C:\Path\Here\Mod.lmlm"
```

## -mods
**Added in an unknown version.**

Makes the Mod Launcher load mods out of the specified path.

```text
-mods "C:\Path\Here"
```

## -noload
**Added in Version 1.18.**

Prevents the Mod Launcher from loading any mods or hacks on startup. This does not prevent them from being loaded with the Reload button.

```text
-noload
```

## -noloadhide
**Added in Version 1.18.**

Makes it so the main window of the Mod Launcher is not hidden while the loading window is visible.

```text
-noloadhide
```

## -noloadingwindowlock
**Added in Version 1.18.**

Makes it so the loading window is not locked to the main window when using `-noloadhide`.

```text
-noloadingwindowlock
```

## -noloadprogress
**Added in Version 1.18.**
	
Makes the Mod Launcher silently load mods and hacks in the background instead of showing the loading window.

This was the default behaviour prior to Version 1.17.

```text
-noloadprogress
```

## -slowload
**Added in Version 1.18.**

Makes the Mod Launcher wait 100ms between each mod or hack that's loaded.

```text
-slowload
```

# Interface
## -nocloselaunchertickbox
**Added in Version 1.21.**

Disables the "Close Launcher" tickbox.

```text
-nocloselaunchertickbox
```

## -nomodslabel
**Added in Version 1.18.1.**

Hides the mods label on the non-Pages view.

```text
-nomodslabel
```

# Language Localisation
## -noselectlanguage
**Added in Version 1.22.4.**

This disables the Mod Launcher's select language dialogue.

```text
-noselectlanguage
```

## -selectlanguage
**Added in Version 1.22.4.**

This forces the Mod Launcher's select language dialogue to always show up on startup.

```text
-selectlanguage
```

# Mod Compilation
## -compile
**Added in an unknown version.**

Specify a mod name to compile.

If the mod does not define an `OutputPath` in the `[Compile]` section of its Meta.ini, you must also use `-outputpath`.

```text
-compile "Donut Mod 4 Beta"
```

**NOTE**: You must use the name of a mod's folder or LMLM file, not its `InternalName`.

## -forceencryption
**Added in Version 1.22.2.**

Makes it so the Mod Launcher will always encrypt mods regardless of their `RequiredLauncher` or other criteria.

```text
-forceencryption
```

## -outputpath
**Added in an unknown version.**

Specify a folder to build the mod(s) to when using `-compile`.

The LMLM file(s) will be named after mod(s) folder.

```text
-outputpath "C:\Path\To\Output\To"
```

# Mods List
## -fullrowselect
**Added in Version 1.18.1.**

Makes the mods list have full row select. This causes various usability issues.

```text
-fullrowselect
```

## -nonmodmods
**Added in Version 1.18.**

Adds a "Non-mods" category to the "General" tab that lets you enable non-mod hacks (such as [[Hacks/CustomFiles/Intro.md]]) as though they are normal mods.

```text
-nonmodmods
```

## -nounreleased
**Added in Version 1.22.**
	
Disables the Unreleased page on the mods list and makes Unreleased mods appear on the other pages they would otherwise be on.

```text
-nounreleased
```

## -saveunreleased
**Added in Version 1.22.**
	
Makes the Mod Launcher save when you're on the "Unreleased" tab when closing the program.

```text
-saveunreleased
```

# Mod Settings
## -ignoredefaultmodsettings
**Added in Version 1.22.**

Makes it so mod settings that were manually set to their default will no longer be bold despite being set.

```text
-ignoredefaultmodsettings
```

## -modsettingsicon
**Added in Version 1.23.10.**

Shows the mod's icon on its settings window.

```text
-modsettingsicon
```

## -modsettingsiconsize
**Added in Version 1.23.10.**

Customise the size of the mod icon when using `-modsettingsicon`. Defaults to 32.

```text
-modsettingsiconsize 32
```

## -noboldsettings
**Added in Version 1.22.**

This makes it so Mod Settings are never displayed in bold.

```text
-noboldsettings
```

## -nomodsettingsresetbutton
**Added in Version 1.23.10.**

Removes the reset button from these windows.

```text
-nomodsettingsresetbutton
```

## -resetdefaultmodsettings
**Added in Version 1.22.**

Makes mod settings get unset when you manually put them back to their default value instead of remaining bold.

```text
-resetdefaultmodsettings
```

## -settings
**Added in an unknown version.**

Launches the Mod Launcher directly into the settings of the specified mod.

As of 1.22, this now includes the current configuration in the Settings window title unless you're using `-notitleconfiguration`.

```text
-settings "Donut Mod"
```

**NOTE**: You must use the name of a mod's folder or LMLM file, not its `InternalName`.

## -vistastylemodsettings
**Added in Version 1.23.10.**

Makes the area above the buttons have a different coloured background with a separator edge in between the two sections.

```text
-vistastylemodsettings
```

## -vistastyleedge
**Added in Version 1.23.10.**

Customise the size of the separator edge `-vistastylemodsettings` when this is enabled.

```text
-vistastyleedge
```

# Shortcuts & Jump Lists
## -forceupdatepinnedshortcuts
**Added in Version 1.22.**

Makes the Mod Launcher always update pinned shortcuts on startup even if they already have an App ID as well as when the running instance does not.

```text
-forceupdatepinnedshortcuts
```

## -nofixpinnedshortcuts
**Added in Version 1.22.**
	
Makes it so the Mod Launcher never updates pinned shortcuts on startup.

```text
-nofixpinnedshortcuts
```

## -nojumplist
**Added in Version 1.22.**

Makes the Mod Launcher clear its jump list on startup.

```text
-nojumplist
```

## -noupdatejumplist
**Added in Version 1.22.**

Makes it so the Mod Launcher will not update its jump lists. 

This disables the **Jump List** tick box on the **Manage Configurations...** window. If a configuration in the Jump List is deleted with this enabled, it will not be removed from the Jump List.

```text
-noupdatejumplist
```

## -updatejumplist
**Added in Version 1.22.**

This makes the Mod Launcher update its jump list even if you use `-noappid`.

```text
-updatejumplist
```

# Update Checking
## -nocheckforupdates
**Added in Version 1.22.4.**

This prevents the Mod Launcher from checking for updates regardless of your setting.

```text
-nocheckforupdates
```

## -noupdatelink
**Added in Version 1.22.**

Hides the update hyperlink on the Main Window added in 1.22.

```text
-noupdatelink
```

## -updatecheckurl
**Added in Version 1.22.4.**

Allows you to override the URL used to check for updates.

Must be on `donutteam.com`, `localhost` or a subdomain of those domains. Prior to Version 1.27, `lucasstuff.com` was also supported.

```text
-updatecheckurl "donutteam.com"
```

## -updatemessage
**Added in Version 1.22.**

Restores the old update message box that was replaced with a hyperlink on the Main Window in 1.22.

```text
-updatemessage
```

# Web Communication
## -noasyncwebrequests
**Added in Version 1.22.3.**

This makes it so all web requests are not asynchronous.

```text
-noasyncwebrequests
```

## -nocurl
**Added in Version 1.17.**

Prevents the Mod Launcher from using [libcurl](https://curl.haxx.se/libcurl/).

```text
-nocurl
```

## -noproxy
**Added in Version 1.22.2.**

Makes the new web requests system added in Version 1.22.2 bypass any system level proxy.

```text
-noproxy
```

## -nossl
**Added in Version 1.17.**

Prevents the Mod Launcher from using SSL (HTTPS).

```text
-nossl
```

## -notls12
**Added in Version 1.17.**

Prevents the Mod Launcher from using TLS 1.2.

```text
-notls12
```

## -proxy
**Added in Version 1.22.4.**

Allows you to define a custom proxy for the Mod Launcher to route through.

```text
-proxy 127.0.0.1
```

## -useragent
**Added in Version 1.18.2.**

Specify a custom user agent for the Mod Launcher.

```text
-useragent "LucasSimpsonsHitAndRunModLauncher/1.19 (Windows NT 6.1; WOW64)"
```

# Windows Environment Check
## -nowindowscheck
**Added in Version 1.25.**

Prevents the Mod Launcher from checking if its running within a Windows environment (actual Windows or Wine).

```
-nowindowscheck
```

## -spoofwindowscheck
**Added in Version 1.25.**

Forces the message that would be shown when the Mod Launcher is not running within a Windows environment to show up. Useful to test localisation of the message.

```
-spoofwindowscheck
```

# Windows XP Service Pack 3 Check
## -forcexpsp3check
**Added in Version 1.23.4.**

Forces the check to happen on non-Windows XP operating systems.

```text
-forcexpsp3check
```

## -noxpsp3check
**Added in Version 1.23.4.**

Disables this check.

```text
-noxpsp3check
```

## -spoofxpsp3check
**Added in Version 1.23.4.**

Forces the message from the check to show up if the check is enabled (either when using Windows XP or when also using `-forcexpsp3check`).

```text
-spoofxpsp3check
```

# Hacks
## -debugloadhacks
**Added in Version 1.19.**

Enables additional console logging from Hack Support when loading hacks.

```text
-debugloadhacks
```

## -loadhackspause
**Added in Version 1.19.**

Pauses the console after all hacks finish loading.

```text
-loadhackspause
```

## -nounrequesthackevents
**Added in Version 1.22.**

Makes it so hacks do not unrequest hack events they're not using after the first time they're told about them resulting in a detriment to the game's performance.

```text
-nounrequesthackevents
```

# Hack: Hack Support
These command line arguments affect [[Hacks/HackSupport.md]].

## -additionalswapchain
**Added in Version 1.23.10.**

Makes this hack make the game use an additional swap chain even when the Resizable Window hack is not enabled.

```text
-additionalswapchain
```

## -noadditionalswapchain
**Added in Version 1.23.10.**

Prevents this hack from making the game use an additional swap chain.

```text
-noadditionalswapchain
```

## -breakgame
**Added in Version 1.22.4.**

Makes it so this hack will break point the game as soon as possible after it gets loaded into it.

As of Version 1.23.2, using this alongside `-suspend` will cause the message shown by `-suspend` to get shown by the Mod Launcher before resuming the injection thread (instead of being shown from inside the game process).

```text
-breakgame
```

## -debugkeybinds
**Added in Version 1.23.6.**

Makes it so this hack will print information about when keybinds are pressed, released and ignored to the console.

This bypasses the "Include > Hacks" setting of the [[Hacks/ConsoleAndLogging.md]] hack.

```text
-debugkeybinds
```

## -debuglookupstring
**Added in Version 1.23.9.**

Makes it so this hack will output to the console every time the game tries looking up a text string.

```text
-debuglookupstring
```

## -debugstagechange
**Added in Version 1.23.8.**

This outputs information to the console when you change stages in a mission.

```text
-debugstagechange
```

## -gameappid
**Added in Version 1.22.**

Makes the game use the same [App ID](https://docs.microsoft.com/en-us/windows/desktop/shell/appids) as the Mod Launcher which results in them sharing a taskbar button instead of appearing separately.

```text
-gameappid
```

## -ignoremissingaddresses
**Added in Version 1.22.**

Makes it so this hack will not assert if Hack Support tries to patch the game, call game code or read/write variables if there is no address for the current game version.

```text
-ignoremissingaddresses
```

## -installallsharedhacks
**Added in Version 1.22.**

Makes the so all shared hacks get installed regardless of whether or not they're actually in use.

```text
-installallsharedhacks
```

## -language
**Added in Version 1.22.4.**

This allows you to override the language of the game:

* **0**: English
* **1**: French
* **2**: German
* **4**: Spanish
 
This doesn't work in the original English release of the game.

This still requires you to provide the dialog RCF for the language you're overriding to.

```text
-language 0
```

As of Version 1.25, this also supports letters as well as the language indices:

* **E**: English
* **F**: French
* **G**: German
* **S**: Spanish

```text
-language E
```

## -msvcasserts
**Added in Version 1.23.6.**

Disables the [custom assert messages](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/Assert_Custom.png) added in 1.23.6, instead this hack will use the [old MSVC style asserts](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/Assert_MSVC.png).

```text
-msvcasserts
```

## -noassertdump
**Added in Version 1.23.6**

Disables the custom assert messages added in 1.23.6 saving a crash dump when they occur.

```text
-noassertdump
```

## -noaudiodevicecheck
**Added in Version 1.22.4.**

Disables an error message added in 1.22.4 that shows up if you try starting the game with no audio devices connected or when the Windows audio service isn't running.

```text
-noaudiodevicecheck
```

## -noblockredundantpresent
**Added in Version 1.23.10.**

Prevents this hack from preventing the game from redundantly presenting (presenting after a previous present or a device reset/swap chain recreation and before beginning a scene) to reduce/prevent flickering when resizing.

```text
-noblockredundantpresent
```

## -noblockredundantreset
**Added in Version 1.23.**

Makes it so this hack does NOT block the game from resetting it Direct3D device when it's unnecessary.

```text
-noblockredundantreset
```

## -nohacklanguagelocalisation
**Added in Version 1.22.4.**

Makes it so hacks do not use language localisation.

```text
-nohacklanguagelocalisation
```

## -nohandlefilenotfound
**Added in Version 1.23.**

Makes it so this hack does not handle the message shown when files are not found, instead showing the game's original message.

```text
-nohandlefilenotfound
```

## -nohardwareskinning
**Added in Version 1.23.**

Disables hardware skinning and instead makes the game use different code for skins.

```text
-nohardwareskinning
```

## -hardwareskinning
**Added in Version 1.23.**

Blocks hacks from disabling hardware skinning.

```text
-hardwareskinning
```

## -nohookd3d
**Added in Version 1.22.**

Disables this hack hooking Direct3D. Enabling this breaks functionality in a great many hacks. Probably don't use this.

```text
-nohookd3d
```

## -hookd3d
**Added in Version 1.23.**

Forces this hack to hook Direct3D regardless of whether any enabled hacks require it to.

```text
-nohookd3d
```

## -nolegacykeys
**Added in Version 1.23.6.**

This disables legacy keybinds.

```text
-nolegacykeys
```

## -noreloadcarcameradata
**Added in Version 1.23.**

Makes it so car camera data does not get reloaded when a car gets loaded (such as when calling it from the phone booth).

```text
-noreloadcarcameradata
```

## -noresourcemeta
**Added in Version 1.22.1.**

Disables Hack Support reading information out of the Meta files for Mods and Hacks.

This makes the Mod Launcher use the internal names of hacks in various places and makes Lua functions that get Meta information (such as [[Hacks/CustomFiles/LuaFunctions/GetModTitle.md]] and [[Hacks/CustomFiles/LuaFunctions/GetModVersion.md]]) return nil.

```text
-noresourcemeta
```

## -suspend
**Added in Version 1.18.2.**

Makes the Mod Launcher suspend the game before its code starts so you can attach a debugger.

As of Version 1.22 the message box now shows up earlier.

As of Version 1.23.2, using this alongside `-breakgame` will cause the message to get shown by the Mod Launcher before resuming the injection thread (instead of being shown from inside the game process).

```text
-suspend
```

# Hack: Anti-aliasing
These command line arguments affect whether or not the [[Hacks/Antialiasing.md]] Anti-aliasing hack will be displayed in the mod's list.

## -forcemsaa
**Added in Version 1.21.**

Makes the launcher show every MSAA mode in the hack's settings regardless of what is supported by your graphics card.

```text
-forcemsaa
```

## -nomsaa
**Added in Version 1.21.**

Makes the launcher skip the check for what MSAA modes are supported which disables and hides this hack from the mods list.

```text
-nomsaa
```

# Hack: Cheat Keys
These command line arguments only take effect when the [[Hacks/CheatKeys.md]] hack is enabled.

## -forceallowcheatkeys
**Added in Version 1.23.5.**

Allows you to opt out of a bunch of other safety checks when pressing keys (such as those added in Version 1.15 and 1.23.5).

```text
-forceallowcheatkeys
```

# Hack: Custom Car Support
These command line arguments only take effect when the [[Hacks/CustomCarSupport.md]] hack is enabled.

## -nocarindexmapping
**Added in Version 1.22.**

Disables the hack dynamically re-mapping car indices to avoid conflicts between mods.

```text
-nocarindexmapping
```

# Hack: Custom Files
These command line arguments only take effect when the [[Hacks/CustomFiles/Intro.md]] hack is enabled.

## -legacyoutput
**Added in Version 1.23.9.**

Reverts the Output Lua function back to how it worked prior to Version 1.23.9.

```text
-legacyoutput
```

## -noadditionalfiles
**Added in Version 1.22.**

Disables the AdditionalFiles folder. This will probably break mods that rely on that folder.

```text
-noadditionalfiles
```

## -noenabledep
**Added in Version 1.23.10.**

Prevents this hack from enabling [Data Execution Prevention](https://docs.microsoft.com/en-us/windows/win32/memory/data-execution-prevention).

```text
-noenabledep
```

## -noluastacktrace
**Added in Version 1.23.8.**

This disables the Lua stack traces added to Lua execution errors in this version.

```text
-noluastacktrace
```

## -notruncateluafilenamestart
**Added in Version 1.23.8.**

This reverts the improvement introduced in this version where Lua errors truncate the start of the path instead of the end of it.

```text
-notruncateluafilenamestart
```

## -slowgameload
**Added in Version 1.22.**

Makes the game wait the specified amount of milliseconds for each byte of any file the game reads to artificially increase load times.

```text
-slowgameload 1000
```

# Hack: Custom Vertex Shader Support
These command line arguments only take effect when the [[Hacks/CustomVertexShaderSupport.md]] hack is enabled.

## -createcustomvertexshadersondevicereset
**Added in Version 1.23.4.**

This makes it so custom vertex shaders are created when the graphics device is created or reset.

```text
-createcustomvertexshadersondevicereset
```

# Hack: Debug Checks
These command line arguments only take effect when the [[Hacks/DebugChecks.md]] hack is enabled.

## -novehiclepositionalsoundplayercarnullcheckasserts
**Added in Version 1.23.6.**

Disables the assert added in this version.

```text
-novehiclepositionalsoundplayercarnullcheckasserts
```

# Hack: Debug Text
These command line arguments only take effect when the [[Hacks/DebugText.md]] hack is enabled.

## -debugtextpage
**Added in Version 1.22.**

Launches the game with a specific debug mode enabled.

**Aliases**: `-debugtextmode`

```text
-debugtextpage "triggers"
```

## -nofitdebugtext
**Added in Version 1.22.**

Disables the debug text being re-sized to fit on the screen.

```text
-nofitdebugtext
```

## -noscaledebugtext
**Added in Version 1.22.**

Disables the debug text being scaled according to the window size.

```text
-noscaledebugtext
```

## -nodebugtextgroups
**Added in Version 1.22.**

Disables grouping of multiple pages registered by a single Mod/Hack.

```text
-nodebugtextgroups
```

# Hack: Direct3D 9
These command line arguments only take effect when the [[Hacks/Direct3D9.md]] hack is enabled.

## -fvf
**Added in Version 1.23.**

Enables support for [fixed function vertex type](https://docs.microsoft.com/en-us/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf).

```text
-fvf
```

## -noqueryd3d9
**Added in Version 1.23.**

Prevents other hacks from accessing or knowing they're running in Direct3D 9.

```text
-noqueryd3d9
```

# Hack: Discord Rich Presence
These command line arguments only take effect when the [[Hacks/DiscordRichPresence.md]] hack is enabled.

## -discordloadinitialise
**Added in Version 1.23.10.**

Makes the hack initialise Discord RPC / GameSDK as soon as the hack loads. This used to be the default behaviour prior to Version 1.22 but it often causes rich presence to not work because Discord handles this poorly.

```text
-discordloadinitialise
```

## -discordrpc
**Added in Version 1.23.10.**

Forces this hack to use Discord RPC even if a Discord GameSDK DLL exists in the DLLs folder.

```text
-discordrpc
```

## -nodiscordregistercommand
**Added in Version 1.23.10.**

Prevents this hack from telling Discord the command to start the Mod Launcher.

```text
-nodiscordregistercommand
```

## -nodiscordrichpresence
**Added in Version 1.23.8.**

This prevents the hack from actually communicating with Discord for testing purposes. It will still output information to the console.

```text
-nodiscordrichpresence
```

# Hack: Lens Flare
These command line arguments only take effect when the [[Hacks/LensFlare.md]] hack is enabled.

## -debugvisibilitytest
**Added in Version 1.19.**

Makes the hack render the Visibility Test mesh instead of the actual lens flare.

```text
-debugvisibilitytest
```

## -deactivatedworldspherelensflares
**Added in Version 1.20.**

Makes Lens Flares inside deactivated World Spheres get enqueued anyways.

```text
-deactivatedworldspherelensflares
```

## -noalpharendertarget
**Added in Version 1.19.**

Makes the hack use a render target that doesn't have an alpha channel. This is noticeable when using `-debugscreenshots`.

```text
-noalpharendertarget
```

## -noocclusion
**Added in Version 1.23.**

Makes it so the hack does not use a occlusion query when the Direct3D 9 hack is enabled.

```text
-noocclusion
```

## -occlusionsleep
**Added in Version 1.23.**

Forces the hack to wait 1 millisecond while waiting for occlusion.

```text
-occlusionsleep
```

# Hack: Load Manager Thread Coordination
These command line arguments affect the [[Hacks/LoadManagerThreadCoordination.md]] hack.

## -radloadmanagermultiplecallbacks
**Added in Version 1.23.2.**

TODO

As of Version 1.23.9, this argument causes the hack to get loaded even if its not enabled in the mods list or required by another hack.

```
-radloadmanagermultiplecallbacks
```

## -radloadmanagerthreadcoordinationimposeframelimit
**Added in Version 1.23.2.**

TODO

As of Version 1.23.9, this argument causes the hack to get loaded even if its not enabled in the mods list or required by another hack.

```
-radloadmanagerthreadcoordinationimposeframelimit
```

# Hack: Modern Computer Support
These command line arguments affect the [[Hacks/ModernComputerSupport.md]] hack.

## -allowzerodeltatime
**Added in Version 1.21.**

Allows the game to exceed 1000 FPS which can cause the delta time to be 0 which can result in the player's position becoming NaN among other issues.

```text
-allowzerodeltatime
```

## -noslowfileloadfixes
**Added in Version 1.25.**

Disables this hack's fixes for slow file loading on Windows Vista / Windows Server 2003 or newer and Wine.

```text
-noslowfileloadfixes
```

## -forceslowfileloadfixes
**Added in Version 1.25.**

Forces this hack's fixes for slow file loading to be enabled.

```text
-forceslowfileloadfixes
```

## -nononenglishwindowsmousebuttonfix
**Added in Version 1.26.**

Disables a fix added in Version 1.26 that addresses an issue in the original game where you can not bind mouse buttons when using a non-English Windows language.

```text
-nononenglishwindowsmousebuttonfix
```

## -noproperclientareacursorcentringandclipping
**Added in Version 1.26.1.**

Disables fixes for an issue where the game incorrectly centered the cursor to the window instead of it's client area *and* an issue where the game assumes the non-client area was 30 pixels at the top and 10 pixels at the other edges when clipping the cursor.

```text
-noproperclientareacursorcentringandclipping
```

# Hack: Modern Resolution Support
These command line arguments affect the [[Hacks/ModernResolutionSupport.md]] hack.

## -noenumresolutions

**Added in Version 1.23.2.**

This stops the Mod Launcher and the hack from getting resolutions from your graphics card.

```text
-noenumresolutions
```

# Hack: NVIDIA Highlights
These command line arguments only take effect when the [[Hacks/NVIDIAHighlights.md]] hack is enabled.

## -nocrashhighlight
**Added in Version 1.23.6.**

Completely disables the type of highlight used when the game crashes.

```text
-nocrashhighlight
```

# Hack: Refraction Shader Support
These command line arguments only take effect when the [[Hacks/RefractionShaderSupport.md]] hack is enabled.

## -refractionmultiplier
**Added in Version 1.23.4.**

Sets a multiplier for the `REFI` parameter on `refract` shaders. This affects how displaced the capture of the screen used in the refraction effect is.

```text
-refractionmultiplier MULTIPLIER
```

## -testrefraction
**Added in Version 1.23.4.**

Makes `refract` shaders always 100% refractive by forcing their `REFB` shader parameters to `1`.

```text
-testrefraction
```

# Hack: Resizable Window
These command line arguments only take effect when the [[Hacks/ResizableWindow.md]] hack is enabled.

## -allowzerowindowsize
**Added in Version 1.23.**

Allows you to resize the client area of the game below 1 pixel on the width or height.

```text
-allowzerowindowsize
```

## -nomaintainwindowcentre
**Added in Version 1.23.**

Prevents this hack from trying to maintain the centre point of the game window when the game resizes it.

```text
-nomaintainwindowcentre
```

# Hack: Screenshots
These command line arguments only take effect when the [[Hacks/Screenshots.md]] hack is enabled.

## -continuousscreenshots
**Added in Version 1.22.**

Makes it so holding the F12 key will rapidly take screenshots.

This was the default behaviour prior to 1.22.

```text
-continuousscreenshots
```

## -debugscreenshots
**Added in Version 1.19.**

Makes the hack save multiple screenshots of a single frame with various differences.

```text
-debugscreenshots
```

# Hack: Sphere Maps
These command line arguments only take effect when the [[Hacks/SphereMaps.md]] hack is enabled.

## -xboxspheremaps
**Added in Version 1.23.4.**

This makes slight tweaks to how the sphere map PDDI shader added by this hack works to make it more like the Xbox version of the game.

```text
-xboxspheremaps
```

# Hack: XInput
These command line arguments only take effect when the [[Hacks/XInput.md]] hack is enabled.

## -ignorepacketnumber
**Added in Version 1.23.**

Makes the hack ignore whether or not the [State packet number](https://docs.microsoft.com/en-au/windows/desktop/api/xinput/ns-xinput-_xinput_state) changed.

```text
-ignorepacketnumber
```

## -nogetstateex
**Added in Version 1.23.**

Makes the hack use [XInputGetState](https://docs.microsoft.com/en-us/windows/desktop/api/xinput/nf-xinput-xinputgetstate) function instead of a similar undocumented function. Using this argument will prevent you from mapping controls to the Guide button.

```text
-nogetstateex
```

## -noxinput
**Added in Version 1.23.1.**
	
This makes it so the hack does not make the game use XInput. 

Despite this seeming counter-intuitive, it would still allow the other features of the hack to work while Windows' XInput-to-DirectInput backwards compatibility handles inputs.

```text
-noxinput
```

## -noxinputdisable
**Added in Version 1.23.1.**

Makes it so XInput does not get disabled when the window is defocused.

```text
-noxinputdisable
```

## -noxinputenable
**Added in Version 1.23.**

Makes it so the hack doesn't call [XInputEnable](https://docs.microsoft.com/en-au/windows/desktop/api/xinput/nf-xinput-xinputenable) if it's available. Instead it will use a function that replicates its functionality (the same one used by default when the function isn't available).

```text
-noxinputenable
```

## -noxinputignoredisconnected
**Added in Version 1.23.9.**

TODO

```text
-noxinputignoredisconnected
```

## -noxinputmaintainorder
**Added in Version 1.23.9.**

TODO

```text
-noxinputmaintainorder
```

## -noxinputremove
**Added in Version 1.23.9.**

TODO

```text
-noxinputremove
```

## -noxinputadd
**Added in Version 1.23.9.**

TODO

```text
-noxinputadd
```