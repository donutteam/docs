* Made it use the new Discord GameSDK instead of the obsolete Discord RPC if the DLL file for it (discord_game_sdk.dll) happens to inexplicably be in the Mod Launcher's DLLs folder.
	* Also added the `-discordrpc` to opt out of this.
	* To be clear, this DLL is not included with the Mod Launcher.
* Fixed an issue when logging state updates after 3:14:07 AM on January 19th, 2038 UTC.
* Made this hack tell Discord the command to start the Mod Launcher so Discord doesn't try launching Simpsons.exe with an incorrect working directory when clicking Play/Play Game.
	* Also added the `-nodiscordregistercommand` command line argument to opt out of this.
		* When using Discord RPC, this causes the old behaviour of Discord updating the command to be wrong.
		* When using Discord GameSDK, this causes Discord to just not update the command.
* Added the `-discordloadinitialise` command line argument. This makes the hack initialise Discord RPC / GameSDK as soon as the hack loads.
	* This used to be the default behaviour prior to Version 1.22 but it often causes rich presence to not work because Discord handles this poorly.