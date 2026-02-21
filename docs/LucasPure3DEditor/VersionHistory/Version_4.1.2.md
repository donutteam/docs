---
title: "Version 4.1.2"
description: "Changelog for Version 4.1.2 of Lucas' Pure3D Editor."
authors: [ 2 ]
---

**This update was released on June 28, 2018.**

* Fixed a crash when copying or cutting a chunk that happened on occasion.
* Fixed a crash when exporting meshes/skins with no UV list.
* Fixed a crash when exporting if an Old Primitive Group references a Shader that doesn't exist.
* Fixed an issue where the **Visible** value inside **State Prop VIsibilites Data** was treated as a block of data instead of an Integer.
* Fixed an issue where Set chunks (Random Textures) were removed when using the Convert to Shop Preview tool.
* Updated the **Edit Rotation** tool to be supported on Skeleton Joint chunks.
* Updated the **Frontend Viewer** to respect the Native X and Native Y values of Sprite chunks.
* Updated the **Locator Editor** and the **Value Editor** to show **Event** and **Parameter** instead of **Unknown** and **Unknown 2** on Type 0 locators.
* Updated the model chunk viewer to show environment maps on Skin chunks with a Version other than 3.
* Updated the **Import Model XML** tool to ignore weights of 0.
* Updated the names of various Chunk types and Chunk values to Radical's official names. If you'd like, you can enable **View > Use Legacy Names** to use the old names.
    * Added a name for **Animated Object Animation** chunks.
    * Added a name for **Animated Object Factory** chunks.
    * Added a name for **Collision Wall** chunks.
    * Added a name for **Lens Flare** chunks.
    * Renamed **Breakable Drawable** to **Anim Obj Wrapper**.
    * Renamed **Breakable Drawable 2** to **Anim Dyna Phys Wrapper**.
    * Renamed **Breakable World Prop** to **Dyna Phys**.
    * Renamed **Breakable World Prop 2** to **Anim Dyna Phys**.
    * Renamed **Cube Shape** to **Road Data Segment**.
    * Renamed **Dynamic World Mesh** to **Anim Coll**.
    * Renamed **Explosion Effect Type** to **Breakable Object**.
        * Renamed **Type** to **Index**.
        * Renamed **Unknown** to **Count**.
    * Renamed **Car Camera Data** to **Follow Camera Data**.
    * Renamed **Ground Collision** to **Intersect**.
    * Renamed **Ground Collision 2** to **Intersect Mesh**.
    * Renamed **Ground Collision 3** to **Intersect Mesh 2**.
    * Renamed **Intersection Locator Node** to **Intersection**.
        * Renamed **Start Intersection Locator Node** to **Start Intersection**.
        * Renamed **End Intersection Locator Node** to **End Intersection**.
    * Renamed **Locator** to **Locator 3**.
    * Renamed **Locator 2** to **Locator**.
    * Renamed **Locator 3** to **Locator 2**.
    * Renamed **Locator 2 Matrix** to **Locator Matrix**.
    * Renamed **Old Particle System** to **Particle System Factory**.
    * Renamed **Particle Emitter Type** to **Inst Particle System**.
    * Renamed **Particle System 2** to **Particle System**.
    * Renamed **Ped Node** to **Path**.
    * Renamed **Prop Instance List** to **Instance List**.
    * Renamed **Random Texture** to **Set**.
    * Renamed **Road Node** to **Road**.
    * Renamed **Road Node 2** to **Road 2**.
    * Renamed **Road Node Segment** to **Road Segment**.
        * Renamed **Cube Shape** to **Road Data Segment**.
    * Renamed **Sector** to **Tree Node 2**.
    * Renamed **Sector Container** to **Tree Node**.
        * Renamed **Axis** to **Split Axis**.
        * Renamed **Position** to **Split Position**.
        * Renamed **Static World Mesh Limit** to **Static Entity Limit**.
        * Renamed **Static World Prop Limit** to **Static Phys Entity Limit**.
        * Renamed **Ground Collision Limit** to **Intersect Entity Limit**.
        * Renamed **Characters, Cars and Breakable World Prop Limit** to **Dyna Phys Entity Limit**.
        * Renamed **Wall Collision Limit** to **Fence Entity Limit**.
        * Renamed **Road Node Segment Limit** to **Road Segment Entity Limit**.
        * Renamed **Ped Node Segment Limit** to **Path Segment Entity Limit**.
        * Renamed **World Mesh Limit** to **Anim Entity Limit**.
    * Renamed **Sector List** to **Tree**.
        * Renamed **World Bounds Maximum** to **Maximum**.
        * Renamed **World Bounds Minimum** to **Minimum**.
    * Renamed **Static Collisionless World Prop** to **Inst Stat Entity**.
    * Renamed **Static Mesh Collision** to **Static Phys**.
    * Renamed **Static World Mesh** to **Static Entity**.
    * Renamed **Static World Prop** to **Inst Stat Phys**.
    * Renamed **Trigger** to **Trigger Volume**.
    * Renamed **Trigger 2** to **Trigger Volume 2**.
    * Renamed **Wall Collision** to **Fence 2**.
    * Renamed **Wall Collision Container** to **Fence**.
    * Renamed **World Effect** to **Particle System 2**.
    * Renamed **World Mesh** to **Anim**.
    * Renamed **World Sky** to **World Sphere**.
    * Updated **ATC**.
        * Renamed **Unknown** to **Classtype Identifier**.
        * Renamed **Unknown 2** to **ATC Entry**.
* Updated the Value Editor to support the following chunk types:
    * Animated Object Animation
    * Animated Object Factory
    * State Prop Callback Data
    * State Prop Event Data
    * State Prop Frame Controller Data
    * State Prop State Data V1