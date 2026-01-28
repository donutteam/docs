* Added the `-hookd3d` command line argument.
* Added the `-nohandlefilenotfound` command line argument.
* Added the `-nohardwareskinning` and `-hardwareskinning` command line arguments.
* Added the `-noreloadcarcameradata` command line argument.
* Fixed an issue where the Direct3D hook in this hack caused the game to reset the Direct3D device redundantly once at startup.
* Made this hack block the game from resetting the Direct3D device when it's not necessary.
    * Also added the `-noblockredundantreset` command line argument to opt out of this.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the hack window procedure event (instead of letting Windows swallow the exception and likely cause corruption).