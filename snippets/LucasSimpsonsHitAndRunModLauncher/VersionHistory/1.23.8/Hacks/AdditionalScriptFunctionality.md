* Made it so this hack actually knows the previous or next stage when starting or ending a stage respectively.
	* In previous versions, the hack just guessed the previous or next stage by subtracting or adding one to the current stage index.
	* The old logic could cause issues in certain cases such as bombbarrel (nuclear waste) stages that can send you back multiple stages.
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetPedsEnabled.md }}