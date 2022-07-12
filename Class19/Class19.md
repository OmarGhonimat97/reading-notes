# Automation

## Python Regular Expressions 

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not.

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import.

> Basic Patterns: Ordinary Characters

You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. 

The (r) at the start of the pattern is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.
For example, \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence.

> Wild Card Characters: Special Characters

Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

Functions namely: search() and group().

With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.
The group function returns the string matched by the re. You will see both these functions in more detail later.

> Repetitions

It becomes quite tedious if you are looking to find long patterns in a sequence. Fortunately, the re module handles repetitions using the following special characters:

- ``` + -```Checks if the preceding character appears one or more times starting from that position.

- ``` * -```Checks if the preceding character appears zero or more times starting from that position.

- ``` ? -```Checks if the preceding character appears exactly zero or one time starting from that position.

- {x} - Repeat exactly x number of times.
- {x,} - Repeat at least x times or more.
- {x, y} - Repeat at least x times but no more than y times.

> Grouping in Regular Expressions

The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are called groups. The parenthesis does not change what the expression matches, but rather forms groups within the matched sequence. 

Another way of doing the same is with the usage of ```<>``` brackets instead. This will let you create named groups. Named groups will make your code more readable. The syntax for creating named group is: ```(?P<name>...)```. Replace the name part with the name you want to give to your group. The ```...``` represent the rest of the matching syntax. 

> Greedy vs. Non-Greedy Matching

When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match". It is the normal behavior of a regular expression, but sometimes this behavior is not desired.

> Summary Table

| Character(s)	 | What it does                                                                                                                                                                                                                                                                                               |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .    | A period. Matches any single character except the newline character.                                                                                                                                                                                                                                       |
| ^	   | A caret. Matches a pattern at the start of the string.                                                                                                                                                                                                                                                     |
| \A		 | Uppercase A. Matches only at the start of the string.                                                                                                                                                                                                                                                      |
| $		  | Dollar sign. Matches the end of the string.                                                                                                                                                                                                                                                                |
| \Z	  | Uppercase Z. Matches only at the end of the string.                                                                                                                                                                                                                                                        |
| [ ]		 | Matches the set of characters you specify within it.                                                                                                                                                                                                                                                       |
| \	   | ∙ If the character following the backslash is a recognized escape character, then the special meaning of the term is taken. <br> ∙ Else the backslash () is treated like any other character and passed through. <br> ∙ It can be used in front of all the metacharacters to remove their special meaning. |
| \w		 | Lowercase w. Matches any single letter, digit, or underscore.                                                                                                                                                                                                                                              |
| \W		 | Uppercase W. Matches any character not part of \w (lowercase w).                                                                                                                                                                                                                                           |
| \s		 | Lowercase s. Matches a single whitespace character like: space, newline, tab, return.                                                                                                                                                                                                                      |
| \S		 | Uppercase S. Matches any character not part of \s (lowercase s).                                                                                                                                                                                                                                           |
| \d	  | Lowercase d. Matches decimal digit 0-9.                                                                                                                                                                                                                                                                    |
| \D		  | Uppercase D. Matches any character that is not a decimal digit.                                                                                                                                                                                                                                            |
| \t		  | Lowercase t. Matches tab.                                                                                                                                                                                                                                                                                  |
| \n		  | Lowercase n. Matches newline.                                                                                                                                                                                                                                                                              |
| \r	   | Lowercase r. Matches return.                                                                                                                                                                                                                                                                               |
| \b	  | Lowercase b. Matches only the beginning or end of the word.                                                                                                                                                                                                                                                |
| +	  | Checks if the preceding character appears one or more times.                                                                                                                                                                                                                                               |
| *	  | Checks if the preceding character appears zero or more times.                                                                                                                                                                                                                                              |
| ?	  | ∙ Checks if the preceding character appears exactly zero or one time. <br>∙ Specifies a non-greedy version of +, *                                                                                                                                                                                         |
| { }	 | Checks for an explicit number of times.                                                                                                                                                                                                                                                                    |
| ( )	 | Creates a group when performing matches.                                                                                                                                                                                                                                                                   |
| < >	 | Creates a named group when performing matches.                                                                                                                                                                                                                                                             |


## shutil - High-level File Operations

The shutil module includes high-level file operations such as copying and archiving.

> Copying Files

copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.

> Copying File Metadata

By default, when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

> Working With Directory Trees

shutil includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.

The symlinks argument controls whether symbolic links are copied as links or as files. The default is to copy the contents to new files. If the option is true, new symlinks are created within the destination tree.

copytree() accepts two callable arguments to control its behavior. The ignore argument is called with the name of each directory or subdirectory being copied along with a list of the contents of the directory. It should return a list of items that should be copied. The copy_function argument is called to actually copy the file.

> Finding Files

The which() function scans a search path looking for a named file. The typical use case is to find an executable program on the shell’s search path defined in the environment variable PATH.

If no file matching the search parameters can be found, which() returns None.

which() takes arguments to filter based on the permissions the file has, and the search path to examine. The path argument defaults to os.environ('PATH'), but can be any string containing directory names separated by os.pathsep. The mode argument should be a bitmask matching the permissions of the file.

> Archives

Python’s standard library includes many modules for managing archive files such as tarfile and zipfile. There are also several higher-level functions for creating and extracting archives in shutil. get_archive_formats() returns a sequence of names and descriptions for formats supported on the current system.

The formats supported depend on which modules and underlying libraries are available, so the output for this example may change based on where it is run.

Use make_archive() to create a new archive file. Its inputs are designed to best support archiving an entire directory and all of its contents, recursively. By default it uses the current working directory, so that all of the files and subdirectories appear at the top level of the archive. To change that behavior, use the root_dir argument to move to a new relative position on the filesystem and the base_dir argument to specify a directory to add to the archive

> File System Space

It can be useful to examine the local file system to see how much space is available before performing a long running operation that may exhaust that space. disk_usage() returns a tuple with the total space, the amount currently being used, and the amount remaining free.

The values returned by disk_usage() are the number of bytes.
