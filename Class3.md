# Read & Write Files in Python
## What Is a File?
Before we can go into how to work with files in Python, it’s important to understand what exactly a file is and how modern operating systems handle some of their aspects.
At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.
Files on most modern file systems are composed of three main parts:
Header: metadata about the contents of the file (file name, size, type, and so on)
Data: contents of the file as written by the creator or editor
End of file (EOF): special character that indicates the end of the file
 
Opening a File
It is done using the open() function. No module is required to be imported for this function.
 
File_object = open(r"File_Name","Access_Mode")

The file should exist in the same directory as the python program file else, full address of the file should be written on place of filename.
Note: The r is placed before filename to prevent the characters in filename string to be treated as special character. For example, if there is \temp in the file address, then \t is treated as the tab character and error is raised of invalid address. The r makes the string raw, that is, it tells that the string is without any special characters. The r can be ignored if the file is in same directory and address is not being placed.
 
 
 
 
File Handle in the file. File handle is like a cursor, which defines from where the data has to be read or written in the file. There are 6 access modes in python.
Read Only (‘r’) : Open text file for reading. The handle is positioned at the beginning of the file. If the file does not exists, raises I/O error. This is also the default mode in which file is opened.
Read and Write (‘r+’) : Open the file for reading and writing. The handle is positioned at the beginning of the file. Raises I/O error if the file does not exists.
Write Only (‘w’) : Open the file for writing. For existing file, the data is truncated and over-written. The handle is positioned at the beginning of the file. Creates the file if the file does not exists.
Write and Read (‘w+’) : Open the file for reading and writing. For existing file, data is truncated and over-written. The handle is positioned at the beginning of the file.
Append Only (‘a’) : Open the file for writing. The file is created if it does not exist. The handle is positioned at the end of the file. The data being written will be inserted at the end, after the existing data.
Append and Read (‘a+’) : Open the file for reading and writing. The file is created if it does not exist. The handle is positioned at the end of the file. The data being written will be inserted at the end, after the existing data.
 
 
 Program to show various ways to read and
 write data in a file.
file1 = open("myfile.txt","w")
L = ["This is Delhi \n","This is Paris \n","This is London \n"] 
  
 \n is placed to indicate EOL (End of Line)

file1.write("Hello \n")

file1.writelines(L)
file1.close() #to change file access modes
  
file1 = open("myfile.txt","r+") 
  
print("Output of Read function is ")
print(file1.read())
print()
  
# seek(n) takes the file handle to the nth
# bite from the beginning.
file1.seek(0) 
  
print( "Output of Readline function is ")
print(file1.readline()) 
print()
  
file1.seek(0)
  
# To show difference between read and readline
print("Output of Read(9) function is ") 
print(file1.read(9))
print()
  
file1.seek(0)
  
print("Output of Readline(9) function is ") 
print(file1.readline(9))
  
file1.seek(0)
# readlines function
print("Output of Readlines function is ") 
print(file1.readlines()) 
print()
file1.close()

Output:
Output of Read function is 
Hello 
This is Delhi 
This is Paris 
This is London 


Output of Readline function is 
Hello 


Output of Read(9) function is 
Hello 
Th

Output of Readline(9) function is 
Hello 

Output of Readlines function is 
['Hello \n', 'This is Delhi \n', 'This is Paris \n', 'This is London \n']

[soures](https://www.geeksforgeeks.org/reading-writing-text-files-python/)


# Exceptions in Python
## Errors and Exceptions
Until now error messages haven’t been more than mentioned, but if you have tried out the examples you have probably seen some. There are (at least) two distinguishable kinds of errors: syntax errors and exceptions.

## Syntax Errors
Syntax errors, also known as parsing errors, are perhaps the most common kind of complaint you get while you are still learning Python:
>>>
>>> while True print('Hello world')
  File "<stdin>", line 1
    while True print('Hello world')
                   ^
SyntaxError: invalid syntax

The parser repeats the offending line and displays a little ‘arrow’ pointing at the earliest point in the line where the error was detected. The error is caused by (or at least detected at) the token preceding the arrow: in the example, the error is detected at the function print(), since a colon (':') is missing before it. File name and line number are printed so you know where to look in case the input came from a script.
# Exceptions
Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. Errors detected during execution are called exceptions and are not unconditionally fatal: you will soon learn how to handle them in Python programs. Most exceptions are not handled by programs, however, and result in error messages as shown here:
>>>
>>> 10 * (1/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>> 4 + spam*3
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'spam' is not defined
>>> '2' + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str

The last line of the error message indicates what happened. Exceptions come in different types, and the type is printed as part of the message: the types in the example are ZeroDivisionError, NameError and TypeError. The string printed as the exception type is the name of the built-in exception that occurred. This is true for all built-in exceptions, but need not be true for user-defined exceptions (although it is a useful convention). Standard exception names are built-in identifiers (not reserved keywords).
The rest of the line provides detail based on the type of exception and what caused it.
The preceding part of the error message shows the context where the exception occurred, in the form of a stack traceback. In general it contains a stack traceback listing source lines; however, it will not display lines read from standard input.
Built-in Exceptions lists the built-in exceptions and their meanings.
 
# Handling Exceptions
It is possible to write programs that handle selected exceptions. Look at the following example, which asks the user for input until a valid integer has been entered, but allows the user to interrupt the program (using Control-C or whatever the operating system supports); note that a user-generated interruption is signalled by raising the KeyboardInterrupt exception.
>>>
>>> while True:
...    try:
...        x = int(input("Please enter a number: "))
...        break
...    except ValueError:
...        print("Oops!  That was no valid number.  Try again...")
...

The try statement works as follows.
First, the try clause (the statement(s) between the try and except keywords) is executed.


If no exception occurs, the except clause is skipped and execution of the try statement is finished.


If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then, if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try/except block.


If an exception occurs which does not match the exception named in the except clause, it is passed on to outer try statements; if no handler is found, it is an unhandled exception and execution stops with a message as shown above.


A try statement may have more than one except clause, to specify handlers for different exceptions. At most one handler will be executed. Handlers only handle exceptions that occur in the corresponding try clause, not in other handlers of the same try statement. An except clause may name multiple exceptions as a parenthesized tuple, for example:
... except (RuntimeError, TypeError, NameError):
...     pass

A class in an except clause is compatible with an exception if it is the same class or a base class thereof (but not the other way around — an except clause listing a derived class is not compatible with a base class). For example, the following code will print B, C, D in that order:
class B(Exception):
    pass

class C(B):
    pass

class D(C):
    pass

for cls in [B, C, D]:
    try:
        raise cls()
    except D:
        print("D")
    except C:
        print("C")
    except B:
        print("B")

Note that if the except clauses were reversed (with except B first), it would have printed B, B, B — the first matching except clause is triggered.
All exceptions inherit from BaseException, and so it can be used to serve as a wildcard. Use this with extreme caution, since it is easy to mask a real programming error in this way! It can also be used to print an error message and then re-raise the exception (allowing a caller to handle the exception as well):
import sys

try:
    f = open('myfile.txt')
    s = f.readline()
    i = int(s.strip())
except OSError as err:
    print("OS error: {0}".format(err))
except ValueError:
    print("Could not convert data to an integer.")
except BaseException as err:
    print(f"Unexpected {err=}, {type(err)=}")
    raise

Alternatively the last except clause may omit the exception name(s), however the exception value must then be retrieved from sys.exc_info()[1].
The try … except statement has an optional else clause, which, when present, must follow all except clauses. It is useful for code that must be executed if the try clause does not raise an exception. For example:
for arg in sys.argv[1:]:
    try:
        f = open(arg, 'r')
    except OSError:
        print('cannot open', arg)
    else:
        print(arg, 'has', len(f.readlines()), 'lines')
        f.close()

The use of the else clause is better than adding additional code to the try clause because it avoids accidentally catching an exception that wasn’t raised by the code being protected by the try … except statement.
When an exception occurs, it may have an associated value, also known as the exception’s argument. The presence and type of the argument depend on the exception type.
The except clause may specify a variable after the exception name. The variable is bound to an exception instance with the arguments stored in instance.args. For convenience, the exception instance defines __str__() so the arguments can be printed directly without having to reference .args. One may also instantiate an exception first before raising it and add any attributes to it as desired.
>>>
>>> try:
...    raise Exception('spam', 'eggs')
... except Exception as inst:
...    print(type(inst))    # the exception instance
...    print(inst.args)     # arguments stored in .args
...    print(inst)          # __str__ allows args to be printed directly,
...                         # but may be overridden in exception subclasses
...    x, y = inst.args     # unpack args
...    print('x =', x)
...    print('y =', y)
...
<class 'Exception'>
('spam', 'eggs')
('spam', 'eggs')
x = spam
y = eggs

If an exception has arguments, they are printed as the last part (‘detail’) of the message for unhandled exceptions.
Exception handlers don’t just handle exceptions if they occur immediately in the try clause, but also if they occur inside functions that are called (even indirectly) in the try clause. For example:
>>>
>>> def this_fails():
...    x = 1/0
...
>>> try:
...    this_fails()
... except ZeroDivisionError as err:
...    print('Handling run-time error:', err)
...
Handling run-time error: division by zero

## Raising Exceptions
The raise statement allows the programmer to force a specified exception to occur. For example:
>>>
>>> raise NameError('HiThere')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: HiThere

The sole argument to raise indicates the exception to be raised. This must be either an exception instance or an exception class (a class that derives from Exception). If an exception class is passed, it will be implicitly instantiated by calling its constructor with no arguments:
raise ValueError  # shorthand for 'raise ValueError()'

If you need to determine whether an exception was raised but don’t intend to handle it, a simpler form of the raise statement allows you to re-raise the exception:
>>>
>>> try:
...    raise NameError('HiThere')
... except NameError:
...    print('An exception flew by!')
...    raise
...
An exception flew by!
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
NameError: HiThere

[soures](https://docs.python.org/3/tutorial/errors.html)

