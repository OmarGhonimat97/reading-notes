I learned basic navigation for moving around the system using the terminal. 
For example the command to enter into a file and view the files in it and move to the previous directory or the home directory also how to access hidden files and directories.
How to search for a specific command also search for the common to do a certain objective.
Creating a file or a directory also deleting them. Also copying a directory which can be very useful in order to keep an original copy when I need to try something or make changes. Also moving a file which works in a similar way as the copy does.
When removing a non-empty file or directory we use -r which means that we do it recursively.

## The Command Line:

In the Bash Command Line Tutorial I learned about the terminal for the linux operating system.
The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.
I open it by typing terminal in the search bar or from the  icon pinned to the taskbar.
Regarding the shell which is a part of the operating system that defines how the terminal behaves, the most common one is called "Bash".
"echo" is the command to view the type of shel you are using.

## Basic Navigation:

This section is about moving around the systems using the command line.
pwd >> Print Working Directory, which indicates your current location.
ls >> List, which displays what the directory contains as a list.
Path of the file is an indication of the file location, whenever we refer to a file or a directory we are referring to its path.
Types of paths are: 
1. Absolute Path >> It specifies the location in relation to the root directory
2. Relative path >> It specifies the location in relation to where we currently are in the system

More on paths:
- ~ (tilda)  >> shortcut to your home directory
- . (dot)  >> reference to your current directory
- .. (dotdot)  >> reference to the parent directory
- cd (change directory) >> without arguments, it will take you back to your home directory, or to the specified directory if wrote with arguments


## More About Files:

***Everything is a file.***
File extension is normally a set of 2-4 characters after the full stop at the end of a file, it indicates the type of the file.

In windows >> the extension is important and the system uses it to determine the file type.

In Linux >> the system ignores the extension and looks inside the file to determine its type.

Linux is case-sensitive while windows for example is case-insensitive.
For spaces in a file and directory names are valid, but it needs attention as in the command line the space is used 
to separate items.

To escape the space issue:
1. Quotes , '' or "", for example to enter a file that has a space in its name >> cd 'Holiday Photos'
2. Escape Characters, which is a backslash (\), the backslash nullifies the special meaning of the next character.

Hidden files in Linux are made by using a dot (.) at the beginning of its name.
The command "ls -a" is used to show the hidden files in a directory.


## Manual Pages:

- man (command to look up) >> manual pages, which are a set of pages which that explain every command available in the system.
To exit the man page press 'q' for quit.
- man -k <search term> >> to search the manual pages containing the search term.
- /(term) >> within a manual page, perform a search for the term.
- n >> after performing a search within a manual page, select the next found item.


## File Manipulation:

Creating a directory:
- mkdir [options] Directory : make directory
- mkdir -p Directory : make parent directory
- mkdir -v Directory : which tells us what it is doing

Removing a directory:
- rmdir [options] Directory : remove a directory
- rmdir -p Directory : remove parent directory
- rmdir -v Directory : which tells us what it is doing

Creating a file:
- touch [options] filename : create a blank file

Copying and moving a file or directory:
- cp [options] source destination : copy a file from a source to a destination
- mv [options] source destination : move a file from a source to a destination

Removing a file and non-empty directories:
- rm [options] file: remove a file
- rm -r : remove a directory and its file recursively

