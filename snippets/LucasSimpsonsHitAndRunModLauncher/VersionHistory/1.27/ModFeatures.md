* Added a new `MaxLength` property to `Text` type `[Setting]` sections in `Meta.ini`.
* Added a new `Multiplayer` property to the `[Miscellaneous]` section in `Meta.ini`
	* This will move move a mod to the new "Multiplayer" tab of the mods list.
* Added the new `KeyCode` type for `[Setting]` sections.
	* While mods can technically declare `KeyCode` settings, there is currently no mechanism for listening for key presses in mods so this is really only usable by mod hacks at this time.
	* Also added a **Clear Keybind** option to the right click menu for this type of setting to remove the current binding entirely.
* Added support for using `RequiredMod` with an `InternalName` declared in a `[LegacyResource]` section.