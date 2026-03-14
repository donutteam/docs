* Added a new check that makes this hack detect and show an error when the game has no handler for a particular file type.
	* This is always enabled because the game *will* crash after this happens.
* Added a new **Missing Detection > Frame Controller Animation/Hierarchy** setting. This detects when a frame controller's animation or hierarchy could not be found.
	* This defaults to **Disabled** because each of Radical's level has about two dozen borked frame controllers and it can be annoying.