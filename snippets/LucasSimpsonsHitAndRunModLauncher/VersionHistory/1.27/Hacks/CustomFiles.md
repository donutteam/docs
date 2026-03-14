### General
* Removed an assert message in this hack that was previously shown if it failed to enable [Data Execution Prevention](https://learn.microsoft.com/en-us/windows/win32/memory/data-execution-prevention).
* Added support for repeating the `[Miscellaneous]`, `[AdditionalFiles]`, `[PathHandlers]` and `[PathRedirections]` sections in `CustomFiles.ini`.
	* If, for some inexplicable reason, already released mods had duplicates of these section headers, they will now be parsed and used instead of being ignored.

### Lua Scripting
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCurrentLevel.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCurrentMission.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/Dialog.md]] function.
	* Also added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/DialogButtons.md]], [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/DialogIcon.md]], and [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/DialogResult.md]] tables.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCurrentSkin.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsRewardUnlocked.md]] function.
	* Also added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/RewardType.md]] table.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/LookupString.md]] Lua function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetActiveLevelMission.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetHighestLevelMission.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCoins.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelFMVUnlocked.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLevelNumCarsPurchased.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLevelNumSkinsPurchased.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLevelNumWaspsDestroyed.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLevelNumGagsCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelMissionCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelStreetRaceCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelBonusMissionCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelWagerRaceCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelGagCompleted.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsPersistentObjectDestroyed.md]] function.
	* Also added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/PersistentObjectSector.md]] table.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsLevelCardCollected.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsCheatEnabled.md]] function.
	* Also added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaTables/Cheat.md]] table.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCurrentCar.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLevelCount.md]] function. 
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCustomSaveDataValue.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/SetCustomSaveDataValue.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetCustomSaveDataValues.md]] function.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetModsWithCustomSaveData.md]] function.