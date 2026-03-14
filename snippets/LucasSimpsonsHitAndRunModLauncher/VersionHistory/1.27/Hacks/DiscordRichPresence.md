* Added a new `ApplicationID` property to the `[Miscellaneous]` section of `DiscordRichPresence.ini` to set a custom application ID.
	* This allows mods to, for example, say "Playing Donut Mod" on Discord instead of "Playing Lucas' Mod Launcher".
* Added the ability to modify what text is shown on a user's Discord profile while playing various types of missions using a new `[States]` section in `DiscordRichPresence.ini`.
* Added the ability to override the entire state text, as well as large image and large image text, on a per mission basis using new mission sections in `DiscordRichPresence.ini`.
* Removed the `-nodiscordrichpresence` [[/LucasSimpsonsHitAndRunModLauncher/CommandLineArguments.md|command line argument]].
* Removed the `[Globals]` section of `DiscordRichPresence.ini`.
	* It was quite limited and the new features added in this version provide all of its functionality and much more.
* Removed the **Show Main Mod** and **Show Mission Elapsed Time** settings.
* Updated the description of this hack.