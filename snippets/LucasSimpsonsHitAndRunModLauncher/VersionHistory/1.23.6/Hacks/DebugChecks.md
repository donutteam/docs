* Added a null-check of the car to the get position and get move speed functions of vehicle positional sound players with a new assert.
    * In other words, this assert can appear after the game tries and fails to play vehicle sounds.
    * Also added the `-novehiclepositionalsoundplayercarnullcheckasserts` command line argument to suppress the assert and allow the game to try to continue.