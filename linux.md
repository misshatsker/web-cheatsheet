***more*** (more namefile)  - is used to view the contents of a file. 

It is called "more" because after it has displayed a page of text, it pauses and puts "-- More --" at the bottom of the screen to let you know that there is more text yet to be shown. To see the next page of text, you just hit the spacebar.
___
***mkdir*** (mkdir namefile)- to create a directory, which is short for "make directory".
___
***mv*** (mv namecategory namedirectory) - To move a file. 

Renaming files is simply a case of "moving" a file from one name to another. For example, to rename file "wolves" to "coyotes", you would type

    mv wolves coyotes

Command can be used to rename directories as well as ***files***. 
___
***ls*** - List the contents of a directory.

***ls -l*** - long listing.
___
***cd*** ( cd namedirectory)- To change directories. 

***cd ..***  - To change to your previous directory.
___
***pwd*** -  To find out where you are, which stands for "print working directory".
___
***cp*** (cp directory/namefile namefile2)- The copy command.
___
***rm*** (rm namefile) - The remove file.

***rmdir*** (rmdir directory) - the remove directory.
___
***File security***

1) The 'r' means you can "read" the file's contents.
2) The 'w' means you can "write", or modify, the file's contents.
3) The 'x' means you can "execute" the file. This permission is given only if the file is a program.

If any of the "rwx" characters is replaced by a '-', then that permission has been revoked.
___
***chmod*** (chmod o+x categoryname) - to change the security permissions on files.

- o -if you want to give "execute" permission to the world ("other") for file "name"
- "+" - you are "adding" a permission.
- x - you are adding "execute" permission.
- categoryname - specify which file you are changing.

 chmod ugo-rwx categoryname - if you want to take all permissions away from everyone.
___
1. "\*" - For example, if you want to execute a command on all files in the current directory, you would specify '*' as the filename.
1. "*ing" - If you want to be more selective and match only files which end in "ing", you would use "*ing"
1. '?' -  It matches exactly one character. For example, if you want to match "sport", but not "spat", you would use "sp??t". The first '?' matches the 'a' in "spat", but the second '?' can't match anything, so "spat" fails.
___

