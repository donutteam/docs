Overhauled the handling of stage vehicles in regards to checkpoints.

This fixes various issues when resuming from a checkpoint when the mission added stage vehicles before it such as:

* Stage vehicles spawning near the origin of the world when activated in the stage with the checkpoint or any subsequent stages without a locator being given to [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ActivateVehicle.md]].
* Stage vehicles that were added but not activated before the checkpoint would not exist if the checkpoint stage did not activate them even though they should.
* Several script functions added by this hack would fail and show an assert when used before the checkpoint:
	* [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/AddStageVehicleCharacter.md]]
	* [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/ResetStageVehicleAbductable.md]]
	* [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetStageVehicleAbductable.md]]
	* [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetStageVehicleAllowSeatSlide.md]]
* Stage vehicles added and activated in the first stage would cause an assert when using the `-testing` command line argument.
	* Only if the checkpoint was not on the first stage (why would you even have one there?)