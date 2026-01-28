* Added a new "mods" page when Debug Text is enabled. This page lists all mods and mod hacks that are enabled.
* Added a `-nounrequesthackevents` command line argument. This makes it so hacks do not unrequest hack events they're not using after the first time they're told about them resulting in reduced efficency.
* Added a `-nohookd3d` command line argument. This disables the Mod Launcher hooking D3D and breaks functionality of numerous hacks. Fun!
* Added new "hacks", "shared hacks" and "hack events" pages that show up in Debug Text when using the `-testing` command line argument.
* Made the `-suspend` command line argument show its message earlier.
* Made the `-testing` command line argument show an assert if the game gets terminated because it took more than 1 second to exit.
* Made it so this hack only installs shared patches when they are necessary.
    * Also added "-installallsharedhacks". This makes all shared patches get installed regardless of whether or not they're actually in use.
* Made this hack show an assert if it tries to patch the game, call game code or read/write variables if there is no address for the current game version.
    * In the case of patches, the patch is also not applied. Otherwise, the game will probably crash after the assert.
    * This should never happen, probably.
    * Anyways, you can use `-ignoremissingaddresses` to disable this assert.