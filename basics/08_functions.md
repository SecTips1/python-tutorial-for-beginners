# Functions in Python
#
# A function is a block of reusable code that runs when called.
# Functions help break down complex problems into smaller, manageable parts and promote code reuse.
#
# In Python, functions are defined using the `def` keyword.

# 1. Defining a Function
# Syntax:
# def function_name(parameters):
#     # code block
#     return [optional value]

def greet():
    print("Hello, World!")

# Calling the function
greet()  # Output: Hello, World!

# 2. Function with Parameters
# You can pass data to a function through parameters.

def greet_with_name(name):
    print(f"Hello, {name}!")

greet_with_name("Alice")  # Output: Hello, Alice!

# 3. Function with Return Value
# Functions can return values using the `return` statement.

def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8

# 4. Default Parameters
# You can assign default values to function parameters, which are used if no argument is passed.

def greet_with_default(name="Stranger"):
    print(f"Hello, {name}!")

greet_with_default()       # Output: Hello, Stranger!
greet_with_default("Bob")  # Output: Hello, Bob!

# 5. Keyword Arguments
# When calling a function, you can specify arguments by their parameter names (keyword arguments).

def describe_person(name, age):
    print(f"{name} is {age} years old.")

describe_person(age=25, name="Alice")  # Output: Alice is 25 years old.

# 6. *args and **kwargs
# You can pass a variable number of arguments to a function using `*args` (for non-keyword arguments)
# and `**kwargs` (for keyword arguments).

def print_numbers(*args):
    for num in args:
        print(num)

print_numbers(1, 2, 3, 4)  # Output: 1 2 3 4 (each number on a new line)

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25)  
# Output:
# name: Alice
# age: 25

# 7. Lambda Functions
# A lambda function is a small anonymous function defined using the `lambda` keyword.
# It can have any number of arguments, but only one expression.

# Example: lambda function to add two numbers
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5
