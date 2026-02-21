---
title: "Version 4.2.1"
description: "Changelog for Version 4.2.1 of Lucas' Pure3D Editor."
authors: [ 2 ]
---

**This update was released on October 5, 2019.**

* Added "New > History" to the "Edit" menu and the right click menu of the tree view.
    * This is only available when "View > Show Advanced Chunks" is enabled.
* Fixed a typo on "Sound Resource Data Name" when viewing ATC chunks.
* Made it so file/folder browse dialogues fall back to Windows XP style versions in the event the Pure3D Editor or .NET fail to create Windows Vista style dialogues.
    * This resolves an issue where this happened on Windows 10 1809 when using a High Contrast theme.
    * This was also able to happen on Windows 7 with "Disable visual themes" ticked in the executable's compatibility settings.
* Made it so "Add History Chunks When Saving" defaults to disabled.
    * These are stripped out of non-decompilable mods by default.
    * These are not visible when "Show Advanced Chunks" is off, in case you've never seen these.
* Made it so the History Chunk Editor only updates the chunk data when defocusing the text field (instead of immediately when typing into it).
* Made it so modifying a history chunk will also update the display name for the chunk in the tree view.
* Made it so the Pure3D Editor will attempt to recover from unhandled exceptions in various cases.
    * Examples include:
        * When making changes to chunks.
        * When saving a file.
            * It should also no longer write invalid files if an exception occurs when writing the file.
        * When updating chunk editors.
        * When updating tools.
        * When updating the tree view of chunks.
    * It is still strongly recommended that in the event of an exception, you use "Save As..." to save your current file to a different location and verify that it still appears to be valid.
* Made it so the Vertex Type in Old Primitive Group chunks get updated automatically when removing lists such as Colour Lists from inside them.
    * In some cases, the game might not like certain lists not existing. This just means that the file will be valid now at least.
    * Loading files that were broken as a result of doing this in an older version of the Pure3D Editor and saving them in this version will fix them.