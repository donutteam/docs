* Made it so the hack will create multiple logs if its unable to write to the log file instead of showing an error message and not logging.
    * In these cases, the hack will just stick a number on the end of the file name like `Log (2).txt`.
* Fixed a crash when failing to open the log file with "Append" ticked.
* Fixed a crash when suppressing RCF files and asyncronous file load requests using Custom Files with this hack enabled and "Include > Hacks" ticked.