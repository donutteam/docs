* Fixed a bug introduced in Version 1.23 where hacks were not notified when the Direct3D device was lost. 
    * This caused a crash when resetting the device (such as when changing the game's resolution) while saving screenshots or after the Lens Flare had been on screen.
        * There may have also been other crashes as a result of this issue.
* Made the crash message include " (C++ exception)" or " (integer division by zero)" after the code if it's one of those types of exceptions.
    * If it's a C++ exception, it also shows the [type name](https://docs.microsoft.com/en-us/cpp/cpp/type-info-class?view=vs-2017), value (if it's a long integer) and the result of [what](https://en.cppreference.com/w/cpp/error/exception/what) (if it's an `std::exception`).
* Made using the `-breakgame` and `-suspend` command line arguments together cause the message from `-suspend` to get shown by the Mod Launcher before resuming the injection thread (instead of being shown from inside the game process).
    * This also prevents the breakpoint from `-breakgame` from happening if there's a debugger attached to the game.