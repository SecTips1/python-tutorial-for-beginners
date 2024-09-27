# 15 Modules

## Introduction
In Python, a module is simply a file containing Python definitions and statements. Modules allow you to logically organize your Python code into separate files, making it more manageable and reusable. A module can contain functions, classes, and variables, and it can also include runnable code.

## Importing Modules
To use a module, you must import it into your script using the `import` statement. Python has a vast standard library of modules, and you can also create your own.

### Example: Importing a Standard Library Module

```python
import math

# Using a function from the math module
result = math.sqrt(16)
print(result)  # Output: 4.0
Importing Specific Functions or Variables
You can import only specific parts of a module by using the from keyword.

from math import sqrt

# Now you can use sqrt() directly without referencing math
result = sqrt(16)
print(result)  # Output: 4.0
Renaming Modules
You can rename modules during import using the as keyword. This is useful to shorten the module name or avoid name conflicts.

import math as m

# Using math module functions with the alias 'm'
result = m.sqrt(16)
print(result)  # Output: 4.0
Creating Your Own Module
You can create your own module by writing Python code in a separate file (e.g., mymodule.py) and then importing it into another script.

Example: Creating a Module (mymodule.py)

# mymodule.py

def greet(name):
    print(f"Hello, {name}!")

pi = 3.14159
Using the Custom Module

import mymodule

# Calling the function from the module
mymodule.greet("Alice")  # Output: Hello, Alice!

# Accessing the variable from the module
print(mymodule.pi)  # Output: 3.14159
Exploring Built-in Modules
Python comes with a large number of built-in modules. You can explore the standard library to find useful modules for your projects. Some popular built-in modules include:

os: Interacting with the operating system.
sys: Accessing system-specific parameters and functions.
random: Generating random numbers.
datetime: Working with dates and times.
json: Parsing and working with JSON data.
Example: Using the os Module

import os

# Get the current working directory
cwd = os.getcwd()
print("Current Working Directory:", cwd)
Importing from a Package
A package is a collection of modules organized in directories that include a special __init__.py file. This file is required to make Python treat the directory as a package.

Example: Importing from a Package
# Assuming we have the following structure:
# mypackage/
# ├── __init__.py
# ├── module1.py
# └── module2.py

from mypackage import module1

# Using functions from module1
module1.some_function()
Reloading a Module
If you make changes to a module and want to see those changes in an already running program, you can reload the module using the importlib.reload() function.

import mymodule
import importlib

# Modify mymodule.py and then reload it
importlib.reload(mymodule)
The dir() Function
The dir() function can be used to list all the functions, variables, and classes defined in a module.

import math

# List all attributes in the math module
print(dir(math))
The __name__ Variable
Each module has a special built-in variable called __name__. When a module is run directly (as a script), the __name__ variable is set to "__main__". This allows you to run code only if the file is executed directly and not when it's imported as a module.

Example:
# mymodule.py

def greet(name):
    print(f"Hello, {name}!")

if __name__ == "__main__":
    # This code runs only if the module is run directly
    greet("Alice")
Conclusion
Modules are an essential feature of Python that allow you to structure your code and reuse functions, variables, and classes across multiple programs. By understanding how to import and create modules, you can write more modular, maintainable, and scalable code.


This Markdown file introduces Python modules, including how to import built-in and custom modules, create your own, explore the standard library, and use packages. It is structured to be visually clear when previewed on GitHub, with examples and explanations that are easy to follow.





