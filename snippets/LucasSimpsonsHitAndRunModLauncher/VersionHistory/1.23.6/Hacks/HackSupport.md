* Added [custom assert messages](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/Assert_Custom.png) that provide more information and save a crash dump.
    * Also added `-msvcasserts` to opt out of this entirely, instead using the [old MSVC style asserts](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/Assert_MSVC.png).
    * Also added `-noassertdump` to opt out of the crash dump specifically.
* Added a "keybinds" debug text mode.
    * This shows all keybinds registered by hacks and their bindings as well as whether or not they're currently pressed or being ignored.
* Added the `-debugkeybinds` command line argument. This makes it so this hack will print information about when keybinds are pressed, released and ignored to the console.
* Added the `-nolegacykeys` command line argument. This disables legacy keybinds.
    * All hacks except Debug Test use a new keybinds system added in Version 1.22 that is not affected by this argument.
        *  These are the ones shown on the new Debug Text page.
    * Debug Test still uses legacy keybinds for most of its functionality so it will get affected by this.
* Made it so the "hacks" debug text mode is available when not using the `-testing` command line argument.
    * By default, it only shows which hacks are loaded. The counts for how many times the various hacks have patched the game still require `-testing`.