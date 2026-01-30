---
title: "Custom Dialogue Character Codes"
description: "This allows mods to define custom dialogue character codes and map multiple outfits to the same character code."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 362 # 1.12
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This allows mods to define custom dialogue character codes and map multiple outfits to the same character code.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomDialogueCharacterCodes
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomDialogueCharacterCodes.ini` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab 1.17 or Later }}
```ini
; [NongenericOutfits] Section: This section is used to assign outfits to Nongeneric Characters.
	; OUTFIT_NAME: Assigns an outfit to a character.

; [CharacterCodes] Section
	; CHARACTER_NAME: Assign a character to a dialogue code.
		; Any outfits assigned to the character in the [NongenericOutfits] list will also work with this character code.

[NongenericOutfits]
; Normal Costume
tny_alt=fattony

; Bonus Mission NPC
b_fattony=fattony

; Car Shop NPC
reward_fattony=fattony

[CharacterCodes]
; Character codes should be 3 or 4 characters.
; This is mainly based on all of Radical's being that way.
fattony=Tony
```
{{ endtab }}
{{ tab Before 1.17 }}
Prior to Version 1.17, `[NongenericOutfits]` had to be assigned to an index in the `[NongenericCharacters]` section.

For backwards compatibility, this method is still supported.

```ini
; [NongenericCharacters] Section
    ; INDEX: The index to assign to a character.
        ; 0-22 are already used by the original game. Any new characters added to this list should use 23 or later.

[NongenericOutfits]
tny_alt=23
b_fattony=23
reward_fattony=23

[NongenericCharacters]
23=fattony

[CharacterCodes]
fattony=Tony
```
{{ endtab }}
{{ endtabs }}

For the default `[NongenericOutfits]`, `[NongenericCharacters]` and `[CharacterCodes]` assignments, see [[/TheSimpsonsHitAndRun/Characters.md]].

# Version History
## Version 1.17.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17.1/Hacks/CustomDialogueCharacterCodes.md }}

## Version 1.17
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomDialogueCharacterCodes.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomDialogueCharacterCodes.md }}