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

So lets start discussing a few Terminoligies.
---
1. "try": This keyword allows the program to run a specific block of code and all the remaining terminologies related to error handling rely on this.
   E.g:
   ```python
   try:
       data = open("file.txt")
   
2. "except": Now incase the piece of code written in the "try" block gives any error, the program will go straight to the except part of the code.
   Referring to our example above, If a file named "file.txt" doesn't exists, the interpreter now moves to the lines shown below.
   E.g:
   ```python
   except:
         data = open("file.txt", "w")
Since in Python, if a file doesnt already exists but it is opened in "write" or "append" mode, it will automatically create that file, this will handle our **FileNotFoundError**.

3. "else": However, if our block of code written inside "try" did indeed worked and didn't provide us with any error, our interpreter will directly jump to the else block, skipping except.
   E.g:
   ```python
   else:
         print(data.read())
4. "finally": The code written inside this block runs no matter what. Your code might or might not give an error in the try block, leading to either the "except" block or "else" block. This
   However doesn't impact finally. E.g:
   ```python
   finally:
           data.close()
   
More on "except"
---
The except keyword is much more useful than this. An example is that in your try block of code, you might encounter several errors, for example an **FileNotFoundError** and a **KeyError**. If you write the except keyword as it is, it will run the code written inside it no matter which error is detected. But if you want to catch only a single type of error, or you want this one "except" to handle only one type of error and another "except" for the other type of error, you can simply write the following:

   ```python
   except FileNotFoundError:
                           data = open("file.txt", "w")
   ```

Some Information regarding **Raise**
---

"raise" is another keyword that you have to get familiar with if you are working with error handling.

Through raise you can create an error by yourself. E.g:

   ```python
   raise TypeError("Forbidden Type Conversion")
```
This will show you an error in your console specifying whatever type and message for that error you have written. 

This can be helpful for you as a developer if:
---

   •Something invalid or unexpected occurs.
   
   •You want to enforce rules.
   
   •You're designing APIs and want others to follow required implementations.
   
   •You want to create more descriptive, domain-specific errors.


