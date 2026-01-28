Fixed an issue where the Pure3D Editor would hang when selecting locators or right clicking on 3D views in some cases with the following changes:
* Made this hack still respond if the game is in a blocking modal loop or minimized while in fullscreen mode.
* Made this hack uninitialise if the game crashes.