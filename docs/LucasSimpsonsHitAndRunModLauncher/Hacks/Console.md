---
title: "Console and Logging"
description: "This hack adds a console and support for log files window that the game, mods and hacks can output to."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 357 # 1.9
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnDeveloperPage.md }}

This hack adds a console and support for log files window that the game, mods and hacks can output to.

# Settings
## Console
### Enabled
Set whether or not the console window enabled.

**Defaults to Enabled.**

### Pause on Exit
Set whether or not the console will pause and say "Press any key to continue..." when the game exits.

**Defaults to Disabled.**

### Include Timestamps
Set whether or not to include timestamps before each thing that is outputted to the console.

**Defaults to Disabled.**

## Logging
### Enabled
Set whether or not logging is enabled.

**Defaults to Disabled.**

### Mode
Set if the hack will log to a single `Log.txt` or a `Logs` folder.

* **Log.txt**: The hack will log to a single file, overwriting it each time (unless **Append** is also enabled).
* **Logs Folder**: The hack will create logs in a folder, creating a new one each time you start the game.

**Defaults to Log.txt.**

### Append
Set if the hack will append new logs to **Log.txt** instead of overwriting it when in that mode.

**Defaults to Disabled.**

### Include Timestamps
Set whether or not to include timestamps before each thing that is logged.

**Defaults to Enabled.**

## Include
### Game
Sets whether or not the games outputs will be shown in the console.

**Defaults to Disabled.**

### Mods
Sets whether or not mod output will be shown in the console.

**Defaults to Enabled.**

### Hacks
Sets whether or not hack output will be shown in the console.

## Include Categories
Sets whether or not to include categories (`[GAME]`, `[MOD]` or `[HACK]`) before each thing that is outputted to the console and logged to the log file.

**Defaults to Disabled.**

# Version History
## Version 1.23.6
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.6/Hacks/Console.md }}

## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/Hacks/Console.md }}

## Version 1.23.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.3/Hacks/Console.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/Console.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/Console.md }}