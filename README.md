# Python-Error-Handling-Notes

While coding in python you might have encountered different type of errors. 

Some may have been deliberate, maybe to check your code on some specific values, while others might have occured without you expecting them.

Below I have listed down some of those erros. You might know some of them from your past experiences, while rest may look unfamiliar to you.

| **Error Name**        | **Simple Definition**                                                                          |
| --------------------- | ---------------------------------------------------------------------------------------------- |
| `SyntaxError`         | Happens when the code is written incorrectly (like missing a colon or parentheses).            |
| `IndentationError`    | Raised when the spaces or tabs used for indentation are incorrect.                             |
| `NameError`           | Happens when you use a variable or function name that hasn’t been defined yet.                 |
| `TypeError`           | Raised when you try to do an operation on the wrong data type (e.g., adding number to string). |
| `ValueError`          | Happens when a function gets the right type but an inappropriate value (e.g., `int("abc")`).   |
| `IndexError`          | Happens when you try to access an invalid index in a list or string.                           |
| `KeyError`            | Raised when you try to access a key that doesn’t exist in a dictionary.                        |
| `AttributeError`      | Happens when you try to use a method or property that doesn’t exist on an object.              |
| `ZeroDivisionError`   | Raised when you try to divide a number by zero.                                                |
| `ImportError`         | Happens when Python can’t find the module you’re trying to import.                             |
| `ModuleNotFoundError` | A specific type of `ImportError` when the module doesn’t exist at all.                         |
| `FileNotFoundError`   | Raised when trying to open a file that doesn't exist.                                          |
| `RuntimeError`        | A generic error that occurs during program execution, usually when nothing else fits.          |
| `RecursionError`      | Happens when a function calls itself too many times without stopping.                          |
| `StopIteration`       | Raised to signal the end of a loop from an iterator.                                           |

Now these errors might trigger you up if you are writing a piece of code with full dedication and suddenly one of these
bad boys pop up to destroy all the Love for coding you have built in years.

However I am writing these notes to help you connect more with these errors.

Instead of Rage Quitting after encountering one of them, I want you to use them yourself.

Doing so will further improve your codes and make them look more professional.

So lets start discussing a few terminoligies.
---
1. "try": This keyword allows the program to run a specific block of code and all the remaining terminologies related to error handling rely on this.
   E.g: try:
             open("file.txt")
   
2. "except": Now incase the piece of code written in the "try" block gives any error, the program will go straight to the except part of the code.
   Referring to our example above, If a file named "file.txt" doesn't exists, the interpreter now moves to the lines shown below.
   E.g: except:
                 open("file.txt", "w")
   Since in Python, if a file doesnt already exists but it is opened in "write" or "append" mode, it will automatically create that file.
