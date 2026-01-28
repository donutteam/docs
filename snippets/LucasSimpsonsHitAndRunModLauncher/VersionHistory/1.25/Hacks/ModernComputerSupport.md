* Made it so this hack always does its fixes for slow file loads when running in Wine regardless of the reported Windows version.
	* This fixes an issue where file loads were slow when Wine was reporting as Windows XP.
		* The Winetricks `dotnet35sp1` verb sets it to do this.
* Added the `-noslowfileloadfixes` command line argument.
* Added the `-forceslowfileloadfixes` command line argument.