* Added an assert when there is a `Condition` or `Conditions` type `[Condition]` section that does not specify any other `[Condition]`s to check.
* Added a new `Setting` type for `[Condition]` sections that allows checking settings of the current mod or other mods.
* Added a new `TiltCamera` `Action` for `[Action]` sections that tilts the camera.
	* The tilt angle can be set with the `Value` property.
	* Also added an optional `Duration` property to set how long it takes the camera to return to normal. 
	* Also added an optional `Reset` property to set if the tilt resets when changing mission.