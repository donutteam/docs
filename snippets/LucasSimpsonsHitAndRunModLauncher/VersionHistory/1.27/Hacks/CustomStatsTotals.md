Now calculates the total amount of story missions, bonus missions, street races, collector cards and movies based on:
* The amount of `Levels` set in the existing `[Miscellaneous]` section.
* The amount of `StoryMissions`, `BonusMissions`, `StreetRaces`, `CollectorCards` and `Movies` set in the new per level `[LevelX]` sections.
* Also added the `IncludeMovieInTotal` property to the new `[LevelX]` section to set whether the level's movie is included in the game total.
* Also added the `RemoveUnusedMissionFromMissionSelect` property to the `Miscellaneous` section to set whether unused missions are included in the mission select menu.