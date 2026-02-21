---
title: "Version 4.2"
description: "Changelog for Version 4.2 of Lucas' Pure3D Editor."
authors: [ 2 ]
---

**This update was released on May 5, 2019.**

* Added a "Two Sided" tickbox to the "Shader Editor".
* Added the "Add Black Magic" tool back to the tools menu that was previously removed in version 4.0.3.
    * It now only shows up if you have "View > Show Advanced Chunks" enabled as Black Magic chunks are Advanced.
    * It also removes all existing Black Magic chunks before adding new ones.
    * The name changed from "Add Magic" since the chunk type was renamed since then.
    * The name also now "(Road Rage)" on the end as these chunks are specific to The Simpsons Road Rage.
* Added the "Export All Intersect" and "Import All Intersect" tools.
    * These tools export and import all intersects in a file to/from OBJ files.
        * These files contain OBJ groups that are separated by surface type.
        * To maintain these, you must make sure you're re-exporting the file with OBJ Groups in your 3D modelling software.
            * In Blender, you would want to make sure [this is ticked](/img/lucaspure3deditor/blender-obj-groups-tickbox.png).
    * The Export tool is only shown if the loaded file contains "Intersect" chunks.
    * The Import tool will remove all intersects in the file and create new ones on the end of the file that are split to fit the standard tree node size.
        * You should keep the original mesh you import somewhere due to the fact it gets split every time you import it.
* Made the "Edit Rotation" tool supported on "Camera" chunks. This might not be useful given that cameras usually have accompanying animations. ¯\_(ツ)_/¯
* Made the Model XML format support alpha for Shaders and Vertex Colours.
* Updated the tool's copyright year to 2019.