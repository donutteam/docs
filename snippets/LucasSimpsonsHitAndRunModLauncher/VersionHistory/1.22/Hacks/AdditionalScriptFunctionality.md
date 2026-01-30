### General
* Fixed an issue introduced in 1.21 where there would be an assert when entering the bonus game.
* Made characters added to cars with ASF commands get removed from and re-added to the world when the car does instead of just when it explodes and is repaired.
    * Characters also now only get added immediately if the car is already in the world.
    * This resolves an issue where characters could remain floating in the air after the game removed a car.
* Made `g_CustomMissionData.empty()` only assert when using the `-testing` command line argument.

### MFK Commands
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/AddParkedCar.md]].
	* This allows you to add a car to the level's parked cars list without needing it to be also added to a traffic group with the [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/AddTrafficModel.md]] command.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/UseTrafficGroup.md]].
	* This sets the current traffic group index when getting to the mission via mission select or restarting it.
	* This does not work unless the DynamicTraffic feature of CustomTrafficSupport is set to `Models` or `Slots`.