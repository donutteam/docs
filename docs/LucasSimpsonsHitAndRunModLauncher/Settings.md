---
title: "Settings"
description: "The Mod Launcher can be configured in various ways."
authors: [ 2 ]
---

The Mod Launcher can be configured in various ways.

# Launcher Settings
To access launcher-level settings:

* **Version 1.26.1 and Older**: Click the **Open...** button and select **Launcher Settings...**.
* **Version 1.27 and Newer**: Open the **File** menu and select **Launcher Settings...**.

## Additional Mods
Here you can add additional folders to load mods from, as well as individual mods.

For **Mods Folders**:
* Use the **Add...** button to browse for a new folder to load mods from.
* Use the **Remove** button to remove the selected folder you previously added.
* Use the **Up** and **Down** buttons to reorder the selected folder in the list.
	* If multiple mods with the same name exist in multiple folders, this will affect which one takes priority.
* Use the **Open** button to open the selected folder in File Explorer.
* Use the **Disabled** tick box to disable a folder in the list, without having to remove it entirely.

For **Individual Mods**:
* Use the **Add...** button to browse for a mod folder or a LMLM file to add.
* Use the **Remove** button to remove the selected mod from the list.
* Use the **Show** button to show the selected mod in File Explorer.
* Use the **Disabled** tick box to disable a mod in the list, without having to remove it entirely.

## Game Tab
Here you can configure various settings related to the game:

* **Executable Path**: The path to your installation of The Simpsons: Hit & Run.
* Crashes
	* **Save Crash Dump**: Makes the Mod Launcher save a crash dump when the game crashes.
		* These can occasionally be helpful to us for debugging issues in the Mod Launcher or mods.
		* To open the **Crashes** folder:
			* **Version 1.26.1 and Older**: Click the **Open...** button and select **Crashes**.
			* **Version 1.27 and Newer**: Open the **File** menu and select **Crashes**.
		* Defaults to Enabled.
	* **Terminate on Crash**: Makes the Mod Launcher immediately terminate the game if it crashes. Not recommended.
		* Defaults to Disabled.
	* **Show Message on Crash**: Makes the Mod Launcher show a message when the game crashes containing the memory address where the crash occurred.
		* As of a Windows 10 update released in April 2018, Microsoft removed the message shown when a program crashes.
		* This is helpful for users running newer versions of Windows, making it easy to know where the game crashed.
		* Defaults to Disabled.
* Advanced
	* **Always Keep Saved Games Separate**: Makes the Mod Launcher use its own separate folder for saved games, even when no Main Mod is enabled.
		* To open the **Saved Games** folder:
			* **Version 1.26.1 and Older**: Click the **Open...** button and select **Saved Games**.
			* **Version 1.27 and Newer**: Open the **File** menu and select **Saved Games**.
		* Defaults to Disabled.
	* **Keep Settings Separate**: Makes the game's `settings.ini` file get stored in a separate location than the game install itself.
		* With this enabled, it will instead be saved to `Documents\My Games\Lucas' Simpsons Hit & Run Mod Launcher\settings.ini`.
		* Defaults to Disabled.
	* **DPI Aware**: Makes the game support different DPI displays on Windows 7 or newer.
		* Defaults to Enabled.
	* **Visual Styles**: Makes messages shown by the game and hacks support Windows visual styles.
		* Defaults to Enabled.
	* **Start in Correct Resolution**: Makes the game start in the correct resolution instead of briefly being in 800x600 before switching to the user's resolution.
		* Defaults to Enabled.
	* **Limit to Single Core**: Limits the game to a single processor core.
		* Defaults to Disabled

## Launcher Tab
Here you can configure various settings for the Mod Launcher itself:

* **Language**: Allows you to choose a language for the Mod Launcher to use on its interface and within certain hacks.
	* Only displayed if additional languages are present in a **Languages** folder next to the Mod Launcher's executable.
	* See [[LanguageLocalisation.md]] for more details.
	* Defaults to English.
* **Check for Updates**: Makes the Mod Launcher send a request to Donut Team on startup to check for updates.
	* Defaults to Enabled.
* **Donut Team Account Integration Support**: Enables [[DonutTeamAccountIntegration.md]].
	* This setting allows you to disable this feature without needing to log out.
	* Defaults to Enabled.
* **Close to Tray**: Makes the Mod Launcher close to a tray icon instead of exiting.
	* Defaults to Disabled.
* **DPI Aware**: Makes the Mod Launcher support different DPI displays on Windows 7 and newer.
	* Defaults to Enabled.
* **Warn on Cloud Directories**: Makes the Mod Launcher detect if the game is installed within a cloud directory, such as Dropbox, Google Drive, OneDrive and iCloud, and show a warning on startup if this is the case.
	* Defaults to Enabled.

## Non-mod Hacks Tab
Here you can find a list of all loaded hacks that are not Mod Hacks and therefore not visible in the Mods List.

# Storage
By default, the Mod Launcher's settings are stored in the Windows Registry. You can find them at the following path:
```
HKEY_CURRENT_USER\Software\Lucas Stuff\Lucas' Simpsons Hit & Run Tools\Lucas' Simpsons Hit & Run Mod Launcher
```

Alternatively, an INI file can be used for storing settings by creating one at the following path:
```
Documents\My Games\Lucas' Simpsons Hit & Run Mod Launcher\Settings.ini
```

Lastly, you can also create a portable install by placing a `Settings.ini` directly next to the Mod Launcher's executable.