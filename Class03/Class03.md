## Reading and Writing Files in Python
### What Is a File?

It contains data which are a set of bytes, this data is organized by a certain format.
It has mainly three parts, Header, Data and End of file (EOF). What this data contains is typically 
represented by the extension of the file for example (.txt).
The file path is a string the indicates the file location, it includes the folder's path, the file name and 
the extension of the file.

Line Endings:
- Unix and Mac >> \n
- Windows >> \r\n

### Opening and Closing a File in Python
- file = open('path') >> to open a file
- file.close() >> to close a file

Closing a file has two ways:
1. try-finally block
2. with statement

Open options:
- 'r' >> Open for reading (default)
- 'w' >> Open for writing, truncating (overwriting) the file first
- 'rb' or 'wb' >> Open in binary mode (read/write using byte data)

#### File objects categories:
- Text files
- Buffered binary files
- Raw binary files

> Text file types

A text file is the most common file. With these types of files, open() will return a 
***TextIOWrapper*** file object.

> Buffered binary file types

A buffered binary file type is used for reading and writing binary files.
With these types of files, open() will return either a ***BufferedReader*** or ***BufferedWriter***
file object.

> Raw file types

A raw file type is generally used as a low-level building-block for binary and text streams.
It is therefore not typically used.
With these types of files, open() will return a ***FileIO*** file object.

### Reading and Writing Opened Files

> Here are the methods for reading a file:

- .read(size=-1) >> This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.
- .readline(size=-1) >> This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.
- .readlines() >> This reads the remaining lines from the file object and returns them as a list.

> Here are the methods for writing a file:

- .write(string) >> This writes the string to the file.
- .writelines(seq) >> This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

> Working with bytes

Sometimes, you may need to work with files using byte strings. This is done by adding the 'b' character to the mode argument. All of the same methods for the file object apply. However, each of the methods expect and return a bytes object instead.

## Exceptions in Python

A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception.

> Exceptions versus Syntax Errors

Syntax errors occur when the parser detects an incorrect statement. 
The arrow indicates where the parser ran into the syntax error.

Exception Error: This type of error occurs whenever syntactically correct Python code results in an error. The last line of the message indicated what type of exception error you ran into.
Instead of showing the message exception error, Python details what type of exception error was encountered.
Python comes with various built-in exceptions as well as the possibility to create self-defined exceptions.

> Raising an Exception

We can use ***raise*** to throw an exception if a condition occurs. The statement can be complemented with a custom exception.
The program comes to a halt and displays our exception to screen, offering clues about what went wrong.

> The ***AssertionError*** Exception

Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We ***assert*** that a certain condition is met.

> The ***try*** and ***except*** Block: Handling Exceptions

The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.
When syntactically correct code runs into an error, Python will throw an exception error. This exception error will crash the program if it is unhandled. The except clause determines how your program responds to exceptions.

> The ***else*** Clause

In Python, using the else statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.

> Cleaning Up After Using ***finally***

Everything in the (finally) clause will be executed. It does not matter if you encounter an exception somewhere in the try or else clauses.

