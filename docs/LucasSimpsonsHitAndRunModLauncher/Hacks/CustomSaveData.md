---
title: "Custom Save Data"
description: "This hack allows other hacks to store custom save data on the end of the save file."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 376 # 1.17
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/AlwaysEnabled.md }}

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/Advanced.md }}

This hack allows other hacks to store custom save data on the end of the save file.

It also always stores extra reward related information on the end of save files. This information is harmless and does not affect save files when they're used in an unmodded copy of the game (though the data will be lost if they're saved over without the hack enabled).

# Version History
## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/CustomSaveData.md }}