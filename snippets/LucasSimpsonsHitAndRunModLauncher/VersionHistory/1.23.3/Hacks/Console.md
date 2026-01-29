* Added support for logging to a file.
    * Also renamed this hack to "Console and Logging" and updated its description to coincide with this addition.
* Made whether or not the console is enabled based on a setting inside the hack instead of whether or not the hack is enabled.
    * Defaults to enabled.
    * This is also to coincide with the new logging feature as they can be enabled independently of one another.
* Made it so this hack hooks the output function used by libpng so it can be affected by the "Include > Game" setting and included in logs.