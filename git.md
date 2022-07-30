***SHA*** -basically an ID number for each commit.
___
***Version Control System / Source Code Manager*** - A version control system (abbreviated as VCS) is a tool that manages different versions of source code. A source code manager (abbreviated as SCM) is another name for a version control system.
___
***Commit*** - Git thinks of its data like a set of snapshots of a mini filesystem. Every time you commit (save the state of your project in Git), it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. You can think of it as a save point in a game - it saves your project's files and any information about them.

Everything you do in Git is to help you make commits, so a commit is the fundamental unit in Git.
___
***Repository / repo*** - A repository is a directory which contains your project work, as well as a few files which are used to communicate with Git. Repositories can exist either locally on your computer or as a remote copy on another computer. A repository is made up of commits.
___
***Working Directory*** - The Working Directory is the files that you see in your computer's file system. When you open your project files up on a code editor, you're working with files in the Working Directory.

This is in contrast to the files that have been saved (in commits!) in the repository.

When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now.
___
***Checkout*** - A checkout is when content in the repository has been copied to the Working Directory.
___
***Staging Area / Staging Index / Index*** - A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.
___
***Branch*** - A branch is when a new line of development is created that diverges from the main line of development. This alternative line of development can continue without altering the main line.
___
***ls*** - used to list files and directories.

***mkdir*** - used to create a new directory.

***cd*** - used to change directories.

***rm*** - used to remove files and directories.
___
***git init*** - To create a new repository with Git. Before you can make commits or do anything else with a git repository, the repository needs to actually exist.

Running the git init command sets up all of the necessary files and directories that Git will use to keep track of everything.
___
***git clone*** - to make an identical copy. You pass a path (usually a URL) of the Git repository you want to clone to the git clone command.

By default will create a directory with the same name as the repository that's being cloned

Can be given a second argument that will be used as the name of the directory

Will create the new repository inside of the current working directory
___
***git status*** - command will display the current status of the repository. 

It will tell us what Git is thinking and the state of our repository as Git sees it.

The git status command will display a lot of information depending on the state of your files, the working directory, and the repository. 
___
***git log*** - The git log command is used to display all of the commits of a repository.

By default, this command displays:

1) the SHA
2) the author
3) the date and the message.
___
***git log --oneline*** -  is used to alter how git log displays information:

This command:

1) lists one commit per line
2) shows the first 7 characters of the commit's SHA
3) shows the commit's message
___
***git log --stat*** - This command:

1) displays the file(s) that have been modified
2) displays the number of lines that have been added/removed
3) displays a summary line with the total number of modified files and lines that have been added/removed
___
***git log -p*** - the -p flag (which is the same as the --patch flag) is used to alter how git log displays information:

This command adds the following to the default output:

1) displays the files that have been modified
2) displays the location of the lines that have been added/removed
3) displays the actual changes that have been made
4) Using the image above, let's do a quick recap of the git log -p output:

- the file that is being displayed
- the hash of the first version of the file and the hash of the second version of the file
not usually important, so it's safe to ignore
- the old version and current version of the file
- the lines where the file is added and how many lines there are
-15,83 indicates that the old version (represented by the -) started at line 15 and that the file had 83 lines
+15,85 indicates that the current version (represented by the +) starts at line 15 and that there are now 85 lines...these 85 lines are shown in the patch below
- the actual changes made in the commit
lines that are red and start with a minus (-) were in the original version of the file but have been removed by the commit
lines that are green and start with a plus (+) are new lines that have been added in the commit.
___
***git show*** - will show only one commit. So don't get alarmed when you can't find any other commits - it only shows one. The output of the git show command is exactly the same as the git log -p command. 

So by default, git show displays:

1) the commit
2) the author
3) the date
4) the commit message
5) the patch information

However, git show can be combined with most of the other flags we've looked at:

- --stat - to show the how many files were changed and the number of lines that were added/removed
- -p or --patch - this the default, but if --stat is used, the patch won't display, so pass -p to add it again
- -w - to ignore changes to whitespace
___
***git add*** - command is used to move files from the Working Directory to the Staging Index.

This command:

1) takes a space-separated list of file names
2) alternatively, the period . can be used in place of a list of files to tell Git to add the current directory (and all nested files)
___
***git commit*** - command takes files from the Staging Index and saves them in the repository.

This command:

- will open the code editor that is specified in your configuration

Inside the code editor:

1) a commit message must be supplied **git commit -m "Initial commit"**
2) lines that start with a # are comments and will not be recorded
3) save the file after adding a commit message
4) close the editor to make the commit

Then, use git log to review the commit you just made!
___
***git diff*** - command can be used to see changes that have been made but haven't been committed, yet. 

This command displays:

1) the files that have been modified
2) the location of the lines that have been added/removed
3) the actual changes that have been made.
___
***.gitignore*** - is used to tell Git about the files that Git should not track. This file should be placed in the same directory that the .git directory is in.

Add this file to your project in the same directory that the hidden .git directory is located. All you have to do is list the names of files that you want Git to ignore (not track) and it will ignore them.

Let's say that you add 50 images to your project, but want Git to ignore all of them. Does this mean you have to list each and every filename in the .gitignore file? Oh gosh no, that would be crazy! Instead, you can use a concept called globbing.

Globbing lets you use special characters to match patterns/characters. In the .gitignore file, you can use the following:

-  blank lines can be used for spacing
- "#" - marks line as a comment
- "*" - matches 0 or more characters
- ? - matches 1 character
- [abc] - matches a, b, _or_ c
- ** - matches nested directories - a/**/z matches
- a/z
- a/b/z
- a/b/c/z
___
