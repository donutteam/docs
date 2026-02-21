---
title: "Version 4.3"
description: "Changelog for Version 4.3 of Lucas' Pure3D Editor."
authors: [ 2, 395 ]
---

**This update was released on February 15, 2020.**

* Fixed an issue on various chunk editors where changes to certain fields would not be saved until they were defocused.
	* This means if you change these values and save the file without defocusing the field, your changes would not actually be saved.
	* This issue applied to the following editors:
		* Trigger Volume Editor
			* Half Extents X/Y/Z
		* Locator Editor
			* Type 7 Locators
				* Right/Up/Front X/Y/Z
			* Type 12 Locators
				* Target Position X/Y/Z
				* Field of View
* Added the Export All Static Entity Models XML tool to the Tools menu.
* Added the ability to import and export Static Entity chunks as Model XML files directly.
	* Previously, you had to import or export the Mesh chunk inside it.
* Fixed an issue where a Skeleton Joint being parented to a child of itself would cause the program to freeze.
* Fixed an issue where a Skeleton Joint being parented to a non-existent Parent would cause an exception when selecting the Skeleton or Composite Drawable.
* Made the Skeleton Hierarchy Viewer show invalid skeleton joints on the end of the list, highlighted in red.
	* Examples of invalid Skeleton Joints include:
		* A joint parented to a joint located after it in the Skeleton.
		* A joint parented to a non-existent joint.
		* A joint parented to a child of itself.
* Updated the tool's copyright year to 2020.
* Added the Flip Fence Normal and Update Fence Normal tools to the right click menu on Fence and Fence 2 chunks.
	* The normal determines the side of the fence that is collidable so these tools make it easy to set it to something valid.
	* The Flip tool inverts the direction of the normal.
	* The Update tool adjusts it to be something valid and should be used after moving the start or end position of the fence.
		* You may need to flip it after doing this to have it be the direction you want.
* Added the Flip All Fence Normals and Update All Fence Normals tools to the Tools menu.
	* These ones are similar to the previous tools except they apply to every Fence in the file.
* Fixed an issue where the tool did not preserve incorrect header sizes in Physics Object chunks when saving.
	* This meant opening some of Radical's original files and saving without making any changes would result in Radical's invalid data being corrected. This critical flaw has now been fixed.
	* This affected the following chunks:
		* l1r1.p3d
			* l1_hedgeunit_Shape
		* l1r2.p3d
			* l1_hedgeunit_Shape
		* l1z2.p3d
			* l1_benchold_Shape
		* l2z4.p3d
			* l2_popsicle_Shape
			* l2_shrubsml_Shape
		* l3z4.p3d
			* l3_krustyglasspost_Shape
		* l4r1.p3d
			* l4_hedgeunit_Shape
		* l4r2.p3d
			* l4_hedgeunit_Shape
		* l4r7.p3d
			* l4r7_cemgravei_Shape
			* l4r7_cemtreeb_Shape
		* l5z4.p3d
			* l5_shrubsml_Shape
		* l6z4.p3d
			* l3_krustyglasspost_Shape
		* l7r1.p3d
			* l7_hedgeunit_Shape
		* l7r2.p3d
			* l7_hedgeunit_Shape
	* Also added an Incorrect Header Size boolean to Physics Object chunks that can be toggled with the Value Editor, in case you want to opt into this for some reason.
	* It should be noted that the game doesn't care if the header size is wrong on these chunks.
* Fixed an issue where the tool did not preserve random data after the null terminator at the end of Dyna Load Data strings in Type 5 locator chunks.
	* This change and the previous one means that saving any of Radical's original uncompressed P3D files should result in exactly the same file.
* Added the Vertex Type Unknown boolean to the Value Editor on Old Primitive Group chunks.
	* This toggles whether or not the Unknown flag is set in the chunk's Vertex Type.
		* This flag is generally not present in The Simpsons Road Rage while it seems to be present in The Simpsons Hit & Run.
		* This change also results in the presence of the flag being preserved when saving the file.
			* Previous versions of the tool would just force the flag to be set.
* Added ellipses to the names of the following tools:
	* Import Model...
	* Export Model...
	* Export All Static Entity Models...
	* Export All Road Rage World Models...
	* Export Model XML...
	* Import Model XML...
	* Export All Intersects...
	* Import All Intersects...
	* Export Language...
	* Import Project...
	* Import Screen...
	* Import Page...
	* Export Project...
	* Export Screen...
	* Export Page...
	* Import Intersect...
	* Export Intersect...
	* Import Image...
	* Export Image...
	* Export All Textures...
	* Export All Sprites...
	* Change Game Path...
	* Edit Rotation...
	* Edit Position...
	* Offset Positions...
* Added the ability to import and export entire P3D files and individual chunks as Lucas' Pure3D Editor Pure3D XML files (.p3dxml).
	* You can import and export the entire file from the Tools menu or by right clicking the root chunk.
		* This gives you the option to append chunks onto the end of the file or replace the contents of the file entirely.
	* You can import and export individual chunks by right clicking them in the hierarchy.
		* This gives you the option to import before and after a chunk as well as the option to replace it.
	* This format contains all of the data in the P3D file.
		* This means you can export a file then import it again to get the exact same file.
	* Also added the ability to open, edit and save as this format just like P3D files.
* Renamed the Import Model and Export Model tools to "Import Model OBJ" and "Export Model OBJ" respectively.
* Renamed the Export All Static Entity Models tool to "Export All Static Entity Models OBJ".
* Moved some items that were previously in the Tools menu to the a new Settings menu:
	* Keep Shared Resources Loaded For Previews
	* Change Game Path...
	* Add History Chunks When Saving
* Removed the empty data value from Export Info chunks.
* Added support for viewing and editing the data inside Export Info Named String and Export Info Named Integer chunks with the Value Editor.
* Fixed a bug where the Copy Car tool was completely broken since its introduction in Version 4.0 in 2015.
	* This was an issue that went seemingly unnoticed for four years.
* Added "Experimental" to the name of the Edit In New Window tool.
	* This feature is and always has been experimental.
* Disabled the Edit In New Window feature on Follow Camera Data chunks.
	* This is because its broken in several different ways when used on these chunks.
	* This might be addressed in a future update.
* Renamed several values on Road chunks.
	* Unknown 2 > Speed
	* Unknown 3 > Intelligence
	* No Reset > Shortcut
		* Supports the Use Legacy Names setting.
* Made the Find References tool support Intersection chunks and Road Data Segment chunks.
* Made it so double clicking boolean values in the Value Editor will toggle between true and false.
* Added an Update Bounds tool to the right click menu on Mesh and Skin chunks.