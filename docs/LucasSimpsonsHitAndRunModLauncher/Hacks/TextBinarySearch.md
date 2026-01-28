---
title: "Text Binary Search"
description: "This hack makes the game's text lookups use a more efficient binary search instead of looking through the entries in order until they find the one they're looking for."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 76 # 1.26
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/AlwaysEnabled.md }}

This hack makes the game's text lookups use a more efficient binary search instead of looking through the entries in order until they find the one they're looking for.

This hack also sorts the text bible loaded out of `srr2.p3d` if it is not already sorted, like how Radical's is by default.