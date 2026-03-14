---
title: "Developer Keys"
description: "This hack adds key binds that are useful for mod developers."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds key binds that are useful for mod developers.

# Settings
## Keybinds
### Toggle Map Debug View
Toggles debug rendering of various types of map data.

**Defaults to F2.**

### Reload Map Regions
Reloads all currently loaded map regions.

**Defaults to F3.**

### Toggle HUD Visibility
Toggles the visibility of the HUD.

**Defaults to F8.**

### Complete Stage
Completes the current mission stage.

**Defaults to F10.**

### Fail Stage
Fails the current mission stage.

**Defaults to Shift+F10.**

### Toggle Text Names
Toggles showing internal names of frontend text strings instead of the actual strings.

**Defaults to Shift+F8.**

# Map Debug Views
What exactly the **Toggle Map Debug View** key does depends on if the [[DebugTest.md]] hack is also enabled.

Without Debug Test, the key simply toggles the game's **Show Tree** [[/TheSimpsonsHitAndRun/Cheats.md|cheat]].

With Debug Test, it cycles through various modes:
* Drawing the current [[/Pure3DFiles/ChunkTypes/Intersect.md]] chunk
* Drawing the current [[/Pure3DFiles/ChunkTypes/Intersect.md]] chunk and current the [[/Pure3DFiles/ChunkTypes/Tree.md]] chunk
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/TriggerVolume.md]] chunks
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Intersection.md]] chunks and [[/Pure3DFiles/ChunkTypes/Road.md]] chunks (without directional arrows)
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Intersection.md]] chunks and [[/Pure3DFiles/ChunkTypes/Road.md]] chunks (with directional arrows)
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Path.md]] chunks
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Fence.md]] chunks

This limitation exists because of how the code of these two hacks is currently structured, but we hope to remove this limitation in a future update.