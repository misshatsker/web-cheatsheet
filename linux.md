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
***groups*** - To get a listing of your group memberships

Notice that you aren't in the "prim" group, but that doesn't matter because you are the owner of these files anyway.
___
***~*** -  to refer to their home directories

For example, if you wanted to copy a file called "jokes" from your home directory to the "/tmp" directory, you could just type

- cp ~/jokes /tmp

You can even use the tilde to specify another user's home directory. If '~' is immediately followed by a User ID, then it no longer refers to your own home directory; it refer's to User ID's home directory. For example, if you wanted to go into bookie's home directory, you could just type

 - cd ~bookie

 Remember that if you put anything after '~' other than '/', Linux will assume that you are referring to another user's home directory.
 ___
 ***man*** - the command which displays portions of this online documentation.

 if you don't know which "ls" option displays hidden files, you can display the manual pages describing "ls" by typing

- man ls

There's an option to "man" which allows you to search for commands which pertain to a particular subject. And how do you figure out which option to "man" allows you to do this? It's simple. Just type

-  man man

1) The heading begins with "man(1)". The "(1)" means that the "man" command is found in Section 1 of the manual
1) NAME contains the name of the command and a brief description of what it does.
1) SYNOPSIS shows the syntax of the command. In the page at right, "[-k]" refers to all of the possible options to the man command. In this case there is only one. The "-k" is surrounded by square brackets because it is an optional part of the command. That is, if you do not include it, the command will still function. The meaning of each option is explained in the OPTIONS section below. Notice the explanation of "-k" at right.

"keyword ..." refers to the possible arguments to the command. Since it is not surrounded by square brackets, it is not optional. That is, you must always include a "keyword" argument to the "man" command. The "..." means that you can specify more than one keyword.

4) DESCRIPTION gives an overview of the purpose of the command.
1) OPTIONS lists all of the possible options and arguments for this command and what they do.
1) SEE ALSO is not of direct importance, but it can be quite useful because it lists commands which have a related purpose.
___
***man -k anyname*** -  to figure out which command is used to spell-check a document.
___
***man finger*** - user information lookup program.
___
***finger name*** - the command which will show you private information.
___
***find***  - to find files. 

(find ~ -name "namefile*") - 

1) The "-name" option says that you are searching for a file's name.
1) "namefile" if you know that is the exact name of the file.
3) '*' - But, if you're not sure whether the file is called "poem", "poems", or even "poem-favorite", then you can use a wildcard. 

However, when you use a wildcard, you need to surround the argument in quotes. If you don't, you will receive a rude error message.
___
***cat*** - to combine files.
___
***'>' or '>>'*** - To send the output from a command such as "cat" to a file. 

For example

- cat jabber wocky > poem

would put the contents of "jabber" and "wocky", one after the other, in a new file called "poem". You can think of the '>' as an arrow pointing to where you want the output to go.

In the above example, if "poem" already exists, then it will be over-written (i.e. it will be deleted before it is recreated). Sometimes that is what you want, but often you will want to keep the previous contents of a file and simply append to it (add to the end of it). This can be accomplished by using '>>' rather than '>'.
___
***"~/name"*** - to create "name" in your home directory, rather than in the current directory. 
___
***lpr*** -  send to printer.

To send your file to a printer called "hp14" rather than the default one, you would type

- lpr -P hp14 thoughts

The '-P' stands for "printer". The printer can have any name that your system administrator chooses, even something like "tower-of-babel", if she feels like it.


***lpq*** - display print queue.

To display all of the print jobs in a different queue, use the '-P' option, just as you would for the "lpr" command. For example, to check on your print job in the "hp14" queue, you would type

- lpq -P hp14

***lprm*** - remove from print queue.

For example, to remove print job 148 from print queue "hp14", you would type

- lprm -P hp14 148
___



