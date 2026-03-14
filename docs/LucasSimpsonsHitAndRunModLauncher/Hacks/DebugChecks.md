---
title: "Debug Checks"
description: "This hack adds various checks and error messages that help with debugging mods."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 376 # 1.17
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnDeveloperPage.md }}

This hack adds various checks and error messages that help with debugging mods.

**Do not enable this hack during casual playthroughs of the base game, it WILL show warning messages at various points where Radical made non-fatal mistakes in their scripts!**

# Settings
## Missing Detection > Locator
Makes the hack show an error message when a locator is not found.

**Defaults to Enabled.**

## Missing Detection > Composite Drawable
Makes the hack show an error message when a composite drawable is not found.

**Defaults to Enabled.**

## Missing Detection > Frame Controller Animation/Hierarchy
Makes the hack show an error message when a frame controller's animation or hierarchy could not be found.

**Defaults to Disabled because each of Radical's levels has about two dozen borked frame controllers.**

## Use Legacy Names
Makes the hack use older, unofficial chunk names.

**Defaults to Disabled.**

## Combine Zone Tree Node Exceeded Messages
Makes the hack combine multiple tree nodes having their limits exceeded into a single message.

**Defaults to Enabled.**

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/Hacks/DebugChecks.md }}

## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/DebugChecks.md }}

## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/DebugChecks.md }}

## Version 1.23.11
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.11/Hacks/DebugChecks.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/DebugChecks.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/DebugChecks.md }}

## Version 1.23.6
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.6/Hacks/DebugChecks.md }}

## Version 1.23.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/DebugChecks.md }}

## Version 1.23.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.3/Hacks/DebugChecks.md }}

## Version 1.22.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.4/Hacks/DebugChecks.md }}

## Version 1.22.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/DebugChecks.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DebugChecks.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DebugChecks.md }}

## Version 1.17.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.2/Hacks/DebugChecks.md }}

## Version 1.17.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.1/Hacks/DebugChecks.md }}