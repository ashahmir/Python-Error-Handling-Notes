# Python-Error-Handling-Notes

While coding in python you might have encountered different type of errors. 

Some may have been deliberate, maybe to check your code on some specific values, while others might have occured without you expecting them.

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
