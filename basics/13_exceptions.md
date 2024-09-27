# 13 Exceptions

## Introduction
Exceptions are events that occur during the execution of a program and disrupt the normal flow of instructions. In Python, exceptions are raised when an error occurs during runtime. Handling exceptions allows your program to continue running or terminate gracefully when unexpected situations occur.

Common exceptions include:
- `ZeroDivisionError`: Occurs when dividing by zero.
- `TypeError`: Raised when an operation or function is applied to an object of an inappropriate type.
- `ValueError`: Raised when a function receives an argument of the correct type but inappropriate value.
- `FileNotFoundError`: Occurs when trying to open a file that does not exist.

## Try-Except Blocks
To handle exceptions, you can use `try-except` blocks. The code inside the `try` block is executed, and if an exception occurs, the code inside the `except` block is executed.

### Example:

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero is not allowed!")
Multiple Exceptions
You can handle multiple types of exceptions by specifying multiple except blocks.

python
Copy code
try:
    value = int("abc")
except ValueError:
    print("Error: Cannot convert to integer!")
except TypeError:
    print("Error: Invalid type!")
Catching All Exceptions
You can catch all exceptions by using a general except block without specifying an exception type. However, this is not recommended unless you have a good reason, as it can mask errors that should be handled differently.

python
Copy code
try:
    # Some code that may raise an exception
    x = 10 / 0
except:
    print("An error occurred!")
Else Block
The else block is executed if no exceptions are raised in the try block. It is useful for code that should only run if the try block is successful.

python
Copy code
try:
    result = 10 / 2
except ZeroDivisionError:
    print("Error: Division by zero!")
else:
    print("Division successful:", result)
Finally Block
The finally block is always executed, whether an exception is raised or not. It is typically used to release resources, such as closing files or network connections.

python
Copy code
try:
    file = open("example.txt", "r")
    # Do something with the file
except FileNotFoundError:
    print("Error: File not found!")
finally:
    file.close()  # This will run whether or not an exception is raised
Raising Exceptions
You can manually raise exceptions using the raise keyword. This is useful when you want to force an exception to occur under certain conditions.

python
Copy code
x = -1
if x < 0:
    raise ValueError("Negative numbers are not allowed!")
Custom Exceptions
You can create custom exceptions by defining a new class that inherits from Python's built-in Exception class.

python
Copy code
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom exception!")
except CustomError as e:
    print(e)
Conclusion
Exception handling is essential for building robust programs that can deal with unexpected situations gracefully. Understanding how to use try-except blocks, raise exceptions, and create custom exceptions will help you write cleaner, more reliable code.

vbnet
Copy code

This Markdown file explains exception handling, including `try-except` blocks, multiple exceptions, the `finally` block, and custom exceptions. It is formatted for clear, visually appealing display on GitHub.





