# 21 Decorators

## Introduction
A decorator in Python is a design pattern that allows you to modify the behavior of a function or class method without permanently modifying its structure. Decorators are commonly used in scenarios where you want to extend or alter the behavior of functions in a reusable and readable way.

### Syntax:
A decorator is applied to a function using the `@` symbol, followed by the name of the decorator function.

```python
@decorator_function
def some_function():
    pass
This is equivalent to:

some_function = decorator_function(some_function)
Basic Decorator Example
Example:
def my_decorator(func):
    def wrapper():
        print("Something before the function.")
        func()
        print("Something after the function.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
Output:
Something before the function.
Hello!
Something after the function.
In this example, the my_decorator function takes say_hello() as an argument, wraps its behavior, and adds functionality both before and after the execution of say_hello().

Decorating Functions with Arguments
Decorators can also be applied to functions that take arguments. To handle this, ensure that the wrapper function accepts *args and **kwargs.

Example:
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Before the function.")
        result = func(*args, **kwargs)
        print("After the function.")
        return result
    return wrapper

@my_decorator
def add(x, y):
    return x + y

result = add(5, 10)
print("Result:", result)
Output:
Before the function.
After the function.
Result: 15
The decorator now works with the add() function, which takes two arguments and returns their sum.

Returning Values from Decorators
Decorators can return values by passing the result of the wrapped function back to the caller.

Example:
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Executing function...")
        result = func(*args, **kwargs)
        print("Function executed.")
        return result
    return wrapper

@my_decorator
def multiply(x, y):
    return x * y

result = multiply(3, 4)
print("Multiplication Result:", result)
Output:
Executing function...
Function executed.
Multiplication Result: 12
In this example, the decorator captures the return value of multiply() and passes it through.

Using Multiple Decorators
You can stack multiple decorators on top of a function by placing multiple @decorator lines above the function definition. The decorators are applied from top to bottom.

Example:
def decorator_one(func):
    def wrapper(*args, **kwargs):
        print("Decorator One")
        return func(*args, **kwargs)
    return wrapper

def decorator_two(func):
    def wrapper(*args, **kwargs):
        print("Decorator Two")
        return func(*args, **kwargs)
    return wrapper

@decorator_one
@decorator_two
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
Output:
Decorator One
Decorator Two
Hello, Alice!
The greet() function is first passed through decorator_two and then through decorator_one.

Decorators with Arguments
Sometimes you need decorators that take arguments. To do this, you create a decorator factory: a function that returns a decorator.

Example:
def repeat(n):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(3)
def say_hi():
    print("Hi!")

say_hi()
Output:
Hi!
Hi!
Hi!
In this example, the repeat() function takes an argument n and returns a decorator that repeats the decorated function n times.

Built-in Python Decorators
Python has several built-in decorators:

@staticmethod: Defines a static method that does not operate on an instance of the class.
@classmethod: Defines a class method that operates on the class itself, not an instance.
@property: Defines a method as a property, allowing access like an attribute.
Example: @staticmethod and @classmethod
class MyClass:
    @staticmethod
    def static_method():
        print("This is a static method.")

    @classmethod
    def class_method(cls):
        print("This is a class method.")

MyClass.static_method()  # Output: This is a static method.
MyClass.class_method()   # Output: This is a class method.
Real-World Use Cases for Decorators
Logging: You can use decorators to log function calls.
Authorization: Decorators can be used to check user permissions before executing a function.
Timing: You can measure the execution time of functions using decorators.
Example: Timing a Function
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"Function took {end_time - start_time:.4f} seconds to execute.")
        return result
    return wrapper

@timer
def long_task():
    time.sleep(2)

long_task()
Output:
vbnet
Copy code
Function took 2.0002 seconds to execute.
Conclusion
Decorators are a powerful feature in Python that allow you to modify the behavior of functions in a clean and readable way. Whether for logging, authorization, timing, or other purposes, decorators can help you write reusable and efficient code. Understanding how to use and create decorators is a key part of mastering Python.


This Markdown file explains Python decorators, including their syntax, usage, and examples of decorators with and without arguments. The file also includes practical use cases, like logging and timing functions, and covers built-in decorators. The content is structured for clarity and readability on GitHub.





