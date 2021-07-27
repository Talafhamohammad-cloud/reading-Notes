# Read & Write Files in Python:

one of the most important thing we can do in python is reading from file and writing on fileWhether it’s writing
to a simple text file, reading a complicated server log, or even analyzing raw byte data .

## What Is a File?

it’s important to understand what exactly a file is and how modern operating systems handle some of their aspects.
a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.
and Files on most modern file systems are composed of three main parts:
**_Header_**: metadata about the contents of the file (file name, size, type, and so on)
**_Data_**: contents of the file as written by the creator or editor
**_End of file (EOF)_**: special character that indicates the end of the file.

# File Paths

When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

1-**_Folder Path_**: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
2-**_File Name_**: the actual name of the file
**_Extension_**: the end of the file path pre-pended with a period (.) used to indicate the file type.

# Line Endings

One problem often encountered when working with file data is the representation of a new line or line ending. The line ending has its roots from back in the Morse Code era, when a specific pro-sign was used to communicate the end of a transmission or the end of a line.

Windows uses the CR+LF characters to indicate a new line, while Unix and the newer Mac versions use just the LF character. This can cause some complications when you’re processing files on an operating system that is different than the file’s source.

# Character Encodings

Another common problem that you may face is the encoding of the byte data. An encoding is a translation from byte data to human readable characters. This is typically done by assigning a numerical value to represent a character. The two most common encodings are the ASCII and UNICODE Formats.
ASCII is actually a subset of Unicode (UTF-8), meaning that ASCII and Unicode share the same numerical to character values. It’s important to note that parsing a file with the incorrect character encoding can lead to failures or misrepresentation of the character. For example, if a file was created using the UTF-8 encoding, and you try to parse it using the ASCII encoding, if there is a character that is outside of those 128 values, then an error will be thrown.

# Opening and Closing a File in Python

When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object: file = open('dog_breeds.txt')
After you open a file, the next thing to learn is how to close it.
It’s important to remember that it’s your responsibility to close the file. In most cases, upon termination of an application or script, a file will be closed eventually. However, there is no guarantee when exactly that will happen. This can lead to unwanted behavior including resource leaks. It’s also a best practice within Python to make sure that your code behaves in a way that is well defined and reduces any unwanted behavior.

# Exceptions in Python:

A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception.

## Exceptions versus Syntax Errors:

Syntax errors occur when the parser detects an incorrect statement.

## Raising an Exception:

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

## The AssertionError Exception:

We assert that a certain condition is met. If this condition turns out to be True, then that is excellent! The program can continue. If the condition turns out to be False, you can have the program throw an AssertionError exception.

## The try and except Block: Handling Exceptions:

The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.
