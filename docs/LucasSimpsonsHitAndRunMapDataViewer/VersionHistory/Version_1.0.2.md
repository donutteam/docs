---
title: "Version 1.0.2"
description: "Changelog for Version 1.0.2 of Lucas' Simpsons Hit & Run Map Data Viewer."
authors: [ 2 ]
---

**This version was released on May 2, 2019.**

* Fixed an issue where positions would be invalid if none of the loaded files (if there are any loaded) contained parts of a map.
* Fixed an issue where the distance shown on the "Measure Roads" tool did not include the distance back to the cursor when clicking down.
* Made it so the program handles corrupted map files more gracefully by showing an informative dialog with an OK button that allows it to continue trying to load the file.
* Made it so you can press Ctrl+C on the main view to copy text. This text is context sensitive.
    * The debug text in the upper left will be copied when on the "Pan" tool (if it's enabled).
    * The position will be copied when on the "Position/Measure" tool when you're not measuring.
    * The length of the line will be copied when on the "Position/Measure" tool when you are measuring.
    * The length of the line will be copied when on the "Measure Roads" tool.
* Made it so you can select a file in the "Loaded files" list and press Ctrl+C to copy the full path to it.