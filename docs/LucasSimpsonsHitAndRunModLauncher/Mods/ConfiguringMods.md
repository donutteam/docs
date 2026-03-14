---
title: "Configuring Mods"
description: "This page has detailed documentation on ways to configure mods."
authors: [ 2 ]
---

This page has detailed documentation on ways to configure mods.

# Structure
These are the various files and folders you can expect to see in the root folder of a mod.

## Meta.ini
This file is the main configuration file for mods. It defines the meta information for the mod, what hacks it requires, who made it and more.

This file must exist and at least contain a `[Miscellaneous]` section to be considered valid. We also strongly recommend that you also at least specify a `Title` and `InternalName` within it.

## Hack Configuration Files
Some Mod Requirable hacks can have or require configuration files in the root of the mod. These can either be `.ini` files or `.xml` files depending on the hack.

## Lua Files
The [[../Hacks/CustomFiles/Intro.md|Custom Files]] hack can have a `CustomFiles.lua` file located in the root of a mod folder.

## Hack Folders
Some Mod Requirable hacks hacks can also utilise folders for their configuration files or resources:

* [[../Hacks/CustomFiles/Intro.md|Custom Files]]
* [[../Hacks/CustomText.md]]

## Icon.png / Icons Folder
Mods can provide icons for the Mod Launcher to use. This can be done as a single 256x256 `Icon.png` file in the root of the mod or as a folder named `Icons` containing any of the following files:

* `16.png`
* `24.png`
* `32.png`
* `48.png`
* `64.png`
* `256.png`

# Configuring Mods
These are all of the available configuration options for mods.
   
These should go in the mod's `Meta.ini`.

## Miscellaneous Section
This section contains a variety of information about the mod itself.

```ini
[Miscellaneous]
; Title
;	The title of the mod that displays in the launcher. 
;	Optional.
Title=Example Mod

; InternalName
;	The internal name of the mod. 
;	This is used for directory names, play history and more. 
;	Optional but strongly recommended.
;	This should not be set to anything that is invalid in a folder name on Windows as this is used for a Main mod's saved games and screenshots folders.
;	Here's a helpful blog post explaining what's not allowed: http://kizu514.com/blog/forbidden-file-names-on-windows-10/
InternalName=ExampleMod

; Description
;	A description of the mod. Use \n for a new line.
;	If RequiredLauncher is set to 1.26 or later, you can repeat this property for new lines instead if you'd prefer.
;	Optional.
Description=An example mod.\nText on another line

; Version
;	Set a version for the mod. 
;	Optional.
Version=1.0

; Category
; 	A category of the mod. Optional.
;	Repeat for multiple categories.
Category=Car Mods
Category=Character Mods

; CommandLine
;   Specify command line arguments to give the game on startup.
;   Can be repeated to specify arguments on separate lines as of 1.23.2
CommandLine=RANDOMBUTTONS

; Main
;	Set whether or not the mod is a main mod. 
;	Gives the mod its own saved games and screenshots folders. 
;	Optional, defaults to 0.
Main=1

; Framework
;	Set whether or not the mod is a framework.
;	This makes it so the mod cannot be enabled on its own.
;	Instead, it must be required by a mod by RequiredFramework.
;	Optional, defaults to 0.
Framework=0

; Disabled
;	Set whether or not the mod is disabled.
;	This will hide the mod from the launcher entirely.
;	Optional, defaults to 0.
Disabled=0

; General
;	Sets whether the Mod appears on the General tab of the Mods List.
;	Defaults to 1 unless Setting, Multiplayer, Developer or Unreleased is also set.
General=1

; Setting
;	Sets whether the mod is on the Settings tab of the Mods List.
;	Optional, defaults to 0.
Setting=0

; Developer
;	Sets whether the mod is on the Developer tab of the Mods List.
;	Optional, defaults to 0.
Developer=0

; Multiplayer
;	Sets whether the Mod appears on the Multiplayer tab of the Mods List.
;	Useful for Multiplayer focused mods.
;	Optional, defaults to 0.
Multiplayer=0

; Unreleased
;	Set whether or not the mod is on the Unreleased tab.
;	Useful to hide secret mods from your main mods list.
;	If set to 1, this will hide the mod from the General, Settings, Developer and Multiplayer pages regardless of the other values.
;	Optional, defaults to 0.
Unreleased=0

; PublicTesting
;	Set whether or not the mod is a public testing build.
;   This is currently handled the same as "Unreleased" except there is not a warning when compiling the mod.
;   Optional, defaults to 0.
PublicTesting=0

; HideFromPlayHistory
;	Hides the mod from Play History and hides the title from Discord Rich Presence.
;	Optional, defaults to 0.
HideFromPlayHistory=0

; SettingsWidth / SettingsHeight
;	Set the width and height of the mod's settings window.
SettingsWidth=200
SettingsHeight=200

; AuthorGroup
;	Define an author group.
;	Repeat for each author group.
;	Not required to use groups but this allows you to control the order.
AuthorGroup=Vehicle Designer
AuthorGroup=Character Designers
AuthorGroup=Frontend Designer

; RequiredHack
;	Require a hack.
;	Repeat for each required hack.
RequiredHack=CustomFiles
RequiredHack=CustomHeadlights

; RequiredMod
;	Require another mod.
;	Repeat for each required mod.
;	The user will have to *manually* enable each required mod when you declare this, so probably don't unless you have a very good reason!
RequiredMod=AnotherMod

; OptionalHack
;	Require a hack if it exists, otherwise this will be ignored.
;	Repeat for each optional hack.
OptionalHack=CustomSomething

; RequiredLauncher
;	Set the minimum required Mod Launcher version for the mod to work.
;	Usually based on which hacks/features the mod requires.
;	Optional but strongly recommended.
RequiredLauncher=1.18

; SupportedMod
;	Forces compatibility between this mod and the specified mod.
;	This mod will override the supported mod. 
;	Repeat for each supported mod.
SupportedMod=3DPhoneBoothPreviews

; ConflictingMod
;	Force a specific mod to conflict with this mod.
;	Recommended only for use where absolutely necessary.
ConflictingMod=SomeModThatBreaksThisOne

; RequiredFramework
;	Require the specified framework to be installed in any mods folder for the mod to work. 
;	Repeat for each required framework.
RequiredFramework=AdditionalCharacters2

; OptionalFramework
;	Require the specified framework if it exists in any mods folder, otherwise will be ignored. 
;	Repeat for each optional framework.
OptionalFramework=AdditionalDynaloadCarModels

; SupportsEnglish
; SupportsDemo
; SupportsInternational
; SupportsBestSellerSeries
;	Set whether or not a mod supports specific versions of the game.
;	Defaults to 1 for all versions except the demo.
SupportsEnglish=1
SupportsDemo=0
SupportsInternational=1
SupportsBestSellerSeries=1

; DefaultLanguage
; DefaultLanguageFrench
; DefaultLanguageGerman
; DefaultLanguageSpanish
;	Set the default language for the CustomText hack for each localization of the game.
;	This is only used if a mod has a CustomText folder with multiple CustomText INI files inside it.
;	Optional.
DefaultLanguage=English
DefaultLanguageFrench=French
DefaultLanguageGerman=German
DefaultLanguageSpanish=Spanish

; Edition
;	Set text that will appear in () after the game's name in the window title.
;	As of 1.21.1, main mods that specify an edition will not have their title pre-pended before the game's name.
Edition=Australian Edition
```

## Description Sections
These sections can be used to have multiple description headers in the Mod information panel.

This type of section can be repeated multiple times.

```ini
[Description]
; Title
;	The title of this description.
Title=Features

; Text
;	The text for this description. Use \n for new lines.
;	If RequiredLauncher in the [Miscellaneous] section is set to 1.26 or later, you can repeat this property for new lines instead if you'd prefer.
Text=- The raddest missions around.\n- The raddest costumes around.\n- More features.
```

## Author Sections
These sections can be used to define information about the author(s) of a mod.

This type of section can be repeated multiple times.

```ini
[Author]
; Name
;	The name of the author.
Name=Loren "Duck" Goodwin

; Website
;	The author's website. Must begin with http:// or https://. 
;	Optional.
Website=https://donutteam.com/

; Notes
;	Extra notes about the author. 
;	Optional.
Notes=A guy who made some things.

; Group
;	The name of the group(s) the author will be listed in.
;	Repeat for each group.
;	Optional.
Group=Vehicle Designers

; Credits
;	Set whether or not the author should be on the Credits tab instead of the About tab. 
;	Optional, defaults to 0.
Credits=0
```

## Setting Sections
These sections can be used to add settings to a mod that can be used when read in [[../Hacks/CustomFiles/Intro.md|Custom Files]] lua scripts with the [[../Hacks/CustomFiles/LuaFunctions/GetSetting.md]] or [[../Hacks/CustomFiles/LuaFunctions/GetSettings.md]] functions.

This type of section can be repeated multiple times.

### General
```ini
[Setting]
; UncompiledOnly
;	Set if the setting will only exist when the mod is not compiled. 
;	This type of setting will be entirely stripped out of the mod is not decompilable.
;	Optional, defaults to 0.
UncompiledOnly=0

; Testing
;	Specify if this setting will only exist when using the "-testing" command line argument on the Launcher itself.
;	Optional, defaults to 0.
Testing=0

; Type: 
;	Specify the type of setting.
; 		MultipleChoice
; 		TickBox
; 		Number
; 		Text
; 		Label
; 		Colour
;		KeyCode
Type=MultipleChoice

; Page 
;	Specify what page the setting is on. 
;	This allows you to organize your settings by pages.
;	Optional.
Page=Gameplay

; Group
;	Specify what group the setting should be in.
;	This allows you to categorize settings further by having groups on pages.
;	Optional.
Group=Car Settings

; Title
;	The display name of the setting. 
;	Defaults to the Name of the setting (unless it's a Label setting where the Title is required).
Title=Default Car

; Tooltip
;	The tooltip to display when hovering over the setting.
Tooltip=This setting allows you select a default car.

; NoReset
;	Specify if the value of the setting will reset when the user resets their settings to the defaults.
;	Optional, defaults to 0.
NoReset=0
```

### MultipleChoice Type Settings
These properties are specific to `MultipleChoice` type settings.

```ini
; Name
;	The internal Name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=DefaultCar

; Option
;	Specify an option for the the MultipleChoice setting.
;	You need to specify at least one Option property OR an Options property (see below)
Option=Family Sedan
Option=Ferrini - Red

; Options
;   Specify the name of a MultipleChoiceSettingOptions section.
;   You need to specify an Options property OR at least one Option property (see above)
Options=SharedOptions

; Text
;	Specify if the value of the setting should be returned as text when requested by CustomFiles.
;	Optional, defaults to 0.
Text=0

; Default
;	The default value of the setting.
;	Optional, defaults to the first Option property or the first Title/Value pair in a referenced MultipleChoiceSettingsOptions section.
Default=0
```

### TickBox Type Settings
These properties are specific to `TickBox` type settings.

```ini
; Name
;	The internal Name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=EnableSomething

; Default
;	The default value of the setting. 0 or 1.
;	Optional, defaults to 0.
Default=0
```

### Number Type Settings
These properties are specific to `Number` type settings.

```ini
; Name
;	The internal Name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=HitAndRunDecay

; Integer
;	Specify whether or not the setting's value has to be an integer.
;	Optional, defaults to 0.
Integer=0

; Min
;	The minimum value of the setting.
;	Optional.
Min=-10.0

; Max
;	The maximum value of the setting.
;	Optional.
Max=10.0

; Default
;	The default value of the setting.
;	Optional, defaults to 0.
Default=0

; NoUpDown
;	Removes the up/down buttons. Only applicable when Integer is set to 1.
;	Optional, defaults to 0.
NoUpDown=0
```

### Text Type Settings
These properties are specific to `Text` type settings.

```ini
; Name
;	The internal Name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=Character

; Password
;	Specify if the textfield should be a password box.
;	Optional, defaults to 0.
Password=0

; Option
;	Specify specific options for the textfield.
;	Optional.
Option=homer
Option=bart
Option=lisa
Option=marge
Option=apu

; Default
;	The default text in the setting.
;	Optional.
Default=homer

; MaxLength
;	The maximum length of the setting's value.
;	Optional, defaults to 32767 (the maximum).
MaxLength=32767
```

### Label Type Settings
These properties are specific to `Label` type settings.

```ini
; Title
;	The text in the Label.
Title=These settings affect some stuff.

; URL
;	Specify a URL to link to from the label text.
;	Must start with http:// or https://.
;	Optional.
URL=https://donutteam.com/
```

### Colour Type Settings
These properties are specific to `Colour` type settings.

```ini
; Name
;	The internal Name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=ColourSetting

; Default
;	The default color.
;	Must start with 0x followed by hexadecimal A,R,G,B values.
Default=0xFFFFFFFF

; Alpha
;	Whether or not this setting should allow an Alpha to be selected.
;	Defaults to 1.
Alpha=1
```

### KeyCode Type Settings
These properties are specific to `KeyCode` type settings.

**Note**: There is not currently any mechanism for mods to actually do anything with KeyCode settings.

```ini
; Name
;	The internal name of the setting.
;	Used when using GetSetting in CustomFiles Lua scripts.
Name=CurrentlyUselessKeyCodeSetting

; Default
;	The default key code.
;	Supports hexadecimal values or human readable strings with modifier keys.
Default=Shift+F3
```

## MultipleChoiceSettingOptions Sections
These sections can be used to define more refined and user friendly options for a `MultipleChoice` type `[Setting]` section.

This type of section can be repeated multiple times and referenced by multiple `MultipleChoice` type `[Setting]` sections.

```ini
; Partial example from the Rebindable Menu Gamepad Inputs hack.

[MultipleChoiceSettingOptions]
; Name
;   Set the name of this section to reference it by in a [Setting] section.
Name=Buttons

; Title/Value Pair
;   Define pairs of Titles and Values for each option in the setting.
Title=-
Value=-1

Title=Z Axis +/LT
Value=4
```

## SettingCondition Sections
These sections can be used to add a condition for a setting being enabled in the Mod Settings window. 

The condition must be true for the setting to be enabled.

This type of section can be repeated multiple times.

```ini
[SettingCondition]
; Type
;	Set the type of condition that must be met for this setting to be enabled.
;		Setting: The condition is based on the value of another setting.
Type=Setting

; Setting
;	The Name of the setting that is affected by this condition.
Setting=AddSkullsToBartsCar

; ConditionSetting
;	The Name of the setting whose value is checked by this condition.
ConditionSetting=EnableMemes

; Operator
;	The operator used to compare the value of the ConditionSetting to the Value inside this SettingCondition.
;		EqualTo
;			You must use this operator when adding a SettingCondition for a TickBox or Text setting.
;		NotEqualTo
;		GreaterThanOrEqualTo
;		LessThanOrEqualTo
;		GreaterThan
;		LessThan
Operator=EqualTo

; Value
;	The value to compare to the value of the Setting.
Value=1
```

## SettingWarning Section
These sections can be used to add warnings for when certain settings are set to certain values.

This type of section can be repeated multiple times.

```ini
[SettingWarning]
; Setting
;	The Name of the setting that the warning checks the value of.
Setting=AddSkullsToBartsCar

; Operator
;	The operator used to compare the value of the Setting to the Value inside this SettingWarning.
;		EqualTo
;			You must use this operator when adding a SettingWarning for a TickBox or Text setting.
;		NotEqualTo
;		GreaterThanOrEqualTo
;		LessThanOrEqualTo
;		GreaterThan
;		LessThan
Operator=EqualTo

; Value
;	The value to compare to the value of the Setting.
Value=1

; Message
;	The message to show when the conditions for the warning are met.
Message=Woah dog, this settings looks like a dank meme. Are you sure you want to enable it?
```

## LegacyResource Sections
These sections are used to declare that the mod supersedes an older Legacy mod.

This is useful for new versions of frameworks that change the InternalName but otherwise maintain compatibility with mods that require it under the old name.

This type of section can be repeated multiple times.

```ini
[LegacyResource]
; InternalName
;	The InternalName of the legacy mod this one is superseding. 
InternalName=AdditionalCharacters

; Title
;	The Title of the legacy mod this one is superseding. Optional.
;	This isn't currently used anywhere but it might be in the future.
Title=Additional Characters
```

## Compile Section
This section is used to define rules for how to compile the mod.

```ini
[Compile]
; OutputPath
;	The path to output the LMLM file to. Optional, if not specified the Launcher will ask when clicking "Compile...".
OutputPath=MyMod.lmlm

; Decompilable
;	Set whether or not the mod is able to be decompiled in the Mods List. Optional, defaults to 0.
Decompilable=0

; ExcludedFileName
;	Files with this name will be excluded when the mod is compiled. 
;	Supports * and ? wildcards.
;	Only applies to files inside the CustomFiles, AdditionalFiles and Resources folders 
;		As of Version 1.14, this also applies to the root folder if your mod is decompilable.
ExcludedFileName=*.bak

; IncludedFileName: 
;	Files with this name will be included when the mod is compiled. 
;	This can be used to include file types that would otherwise be excluded.
;	Supports * and ? wildcards.
;	Only applies to files inside the CustomFiles, AdditionalFiles and Resources folders 
;		As of Version 1.14, this also applies to the root folder if your mod is decompilable.
IncludedFileName=Something.txt

; ExcludedFolderName
;	Folders with this name will be excluded when the mod is compiled. 
;	Supports * and ? wildcards.
;	Only applies to folders inside the CustomFiles, AdditionalFiles and Resources folders 
;		As of Version 1.14, this also applies to the root folder if your mod is decompilable.
ExcludedFolderName=_Assets

; IncludedFolderName: 
;	Folders with this name will be included when the mod is compiled.
;	This can be used to include folders that would otherwise be excluded.
;	Supports * and ? wildcards.
;	Only applies to folders inside the CustomFiles, AdditionalFiles and Resources folders 
;		As of Version 1.14, this also applies to the root folder if your mod is decompilable.
IncludedFolderName=Resources2OrSomething

; MinifyArt
;	Set whether or not to minify .p3d files (removes history chunks) when the mod is compiled. 
;	Defaults to 1 unless the mod is Decompilable.
MinifyArt=1

; MinifyPNGs
;	Set whether or not to minify .png files (removes unrequired data such as Adobe Fireworks data) when the mod is compiled.
;	Defaults to 1 unless the mod is Decompilable.
MinifyPNGs=1

; MinifyXMLs
;   Set whether or not to minify .xml files.
;   Defaults to 1 unless the mod is Decompilable.
MinifyXMLs=1

; IncludeHidden
;	Set whether or not to include hidden files and folders. 
;	Defaults to 0 unless the mod is Decompilable.
IncludeHidden=0

; IncludeModifiedDates
;	Set whether or not to preserve modified dates on files and folders. 
;	Defaults to 0 unless the mod is Decompilable.
IncludeModifiedDates=0

; IncludeEmptyFolders: 
;	Set whether or not to include empty folders. 
;	Defaults to 0 unless the mod is Decompilable.
IncludeEmptyFolders=0

; RewriteMetaINI
;	Set whether or not to rewrite Meta.ini when compiling the mod.
;	Defaults to 0 unless the mod is Decompilable.
RewriteMetaINI=1

; Encryption
;	Set whether or not the mod should be encrypted when it's compiled.
;	Only text based files (.ini, .xml, .lua, .con, .mfk, .cho, .spt) get encrypted by default.
;	Defaults to 1 if the mod is not Decompilable and has its RequiredLauncher set to 1.22.2 or newer.
Encryption=1

; NonencryptedFileName
;	Specify a file name that will not be encrypted regardless of other factors.
NonencryptedFileName=*.spt	; Don't encrypt any SPT files.

; EncryptedFileName
;	Specify a file name that will be encrypted regardless of other factors.
EncryptedFileName=*.p3d	; Encrypt all P3D files, probably not ideal.

; EncryptionMaximumSize
;	Specify the maximum file size that will make files get encrypted in bytes.
EncryptionMaximumSize=1024000	; Encrypt everything that's 100KB or under.
```

# Version History
## Version 1.27
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.27/ModFeatures.md }}

## Version 1.26
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/ModFeatures.md }}

## Version 1.25.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/ModFeatures.md }}

## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/ModFeatures.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/ModFeatures.md }}

## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/ModFeatures.md }}

## Version 1.23.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.3/ModFeatures.md }}

## Version 1.23.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/ModFeatures.md }}

## Version 1.22.3
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/ModFeatures.md }}

## Version 1.22.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.2/ModFeatures.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/ModFeatures.md }}

## Version 1.20.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.1/ModFeatures.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/ModFeatures.md }}

## Version 1.16
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.16/ModFeatures.md }}

## Version 1.15.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15.1/ModFeatures.md }}

## Version 1.15
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.15/ModFeatures.md }}

## Version 1.14
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.14/ModFeatures.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/ModFeatures.md }}

## Version 1.12.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12.1/ModFeatures.md }}

## Version 1.12
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12/ModFeatures.md }}