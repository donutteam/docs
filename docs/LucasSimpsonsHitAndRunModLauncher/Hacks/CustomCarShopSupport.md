---
title: "Custom Car Shop Support"
description: "This hack allowed mods to define custom car shop NPCs and conversation names."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 362 # 1.12
removedVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
  superseded_by: "LucasSimpsonsHitAndRunModLauncher/Hacks/CustomShopSupport.md"
---

This hack allowed mods to define custom car shop NPCs and conversation names.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomCarShopSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomCarShopSupport.ini` and add the parameters necessary for your mod inside it.

```ini
; [LevelX] Section
    ; Conversation: The name of the conversation to use.
        ; Leave blank to have no conversation.
    ; Character: The name of the character to use.

; Simply make a section for whichever levels you want to modify.

[Level1]
; The new conversation name to use
Converation=salad

; The new character to use including the "reward_" prefix applied to car shop NPCs
Character=reward_krusty

[Level4]
; If you don't want a conversation, you can just set it to nothing
Conversation=
```