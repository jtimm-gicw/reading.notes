# 401-Terminal_Info

## Thoughts

### Command Line
It was a general overview of what the command line is and some simeple commands like *bash*.  Most of the information there, I feel I know well already because I use it everyday.

### Basic Navigation
This sectioned discussed how to move in and out of files with "cd",  It also discussed "ls" to list what files are in that particular directory you are in. There are 2 types of paths we can use, *absolute and relative*. Absolute paths specify a location (file or directory) in relation to the root directory. Relative paths specify a location (file or directory) in relation to where we currently are in the system. It also explained about the **"root"** directory, which I think of as the "base" where the "file tree" grows from and branching out into files and folders.

### More about files
linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc.  Linux the system actually ignores the extension and looks inside the file to determine what type of file it is.  Windows are case insensitive when it comes to referring to files. Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.  No spaces in file names.  Use ".", "-", "_" instead of a space. method is to use what is called an escape character, which is a backslash ( \ ).  the backslash escapess (or nullify) the special meaning of the next character.  To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.


### Manual pages
The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept. It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve. To be effective with this approach, you may need a few goes. It is not uncommon to find that a particular word exists in many manual pages. If you want to search within a manual page this is also possible. To do this, whilst you are in the particular manual page you would like to search press forward slash '/' followed by the term you would like to search for and hit 'enter' If the term appears multiple times you may cycle through them by pressing the 'n' button for next.


### File manipulation 
Creating a directory is pretty easy. The command we are after is **mkdir** which is short for Make Directory. The -p which tells mkdir to make parent directories as needed.  -v which makes mkdir tell us what it is doing. The command to remove a directory is rmdir, short for remove directory. To create blank files using the command **touch**. Before changing something, we may wish to create a duplicate so that if something goes wrong we can easily revert back to the original. The command we use for this is **cp** which stands for *copy*.  To move a file we use the command mv which is short for move.  The command to remove or delete a file is **rm** which stands for remove. **-r** similar to cp it stands for *recursive*. When rm is run with the -r option it allows us to remove directories and all files and directories contained within.


### Cheat Sheet
[https://ryanstutorials.net/linuxtutorial/cheatsheet.php]


