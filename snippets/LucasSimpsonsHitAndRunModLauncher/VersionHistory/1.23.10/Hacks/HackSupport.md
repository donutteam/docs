* Made the game use an additional swap chain when using the Resizable Window hack in windowed mode to make resizing smoother.
	* Also added the `-noadditionalswapchain` command line argument to opt out of this.
	* Also added the `-additionalswapchain` command line argument to force this when the Resizable Window hack is not enabled.
		* This should technically make changing the resolution with the in-game menus slightly faster.
* Made the hack prevent the game from redundantly presenting (presenting after a previous present or a device reset/swap chain recreation and before beginning a scene) to reduce/prevent flickering when resizing.
	* Also added the `-noblockredundantpresent` command line argument to opt out of this.
* Fixed an issue where the game window would be redrawn when resizing when the Resizable Window hack was enabled and its Present While Resizing setting was ticked if the game window's icon was being changed to that of a main/edition mod.
* Fixed an issue where all created vertex shaders would be leaked when blocking a redundant Direct3D device reset.
* Fixed an issue where `..` wasn't handled in file paths since Version 1.10 when using the Legacy Virtual File System (via `-legacyfilesystem` as of Version 1.22).
	* This fixes an issue where mods may have been able to access files outside of directories mounted within the Virtual File System.