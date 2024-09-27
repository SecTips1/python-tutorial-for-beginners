# 18 Lambdas

## Introduction
In Python, a lambda function is a small, anonymous function defined using the `lambda` keyword. Unlike normal functions defined with `def`, lambda functions can have only one expression and are typically used for short, simple operations. They are useful when you need a small function for a short period of time and don’t want to define a full function using `def`.

### Syntax:
```python
lambda arguments: expression
The lambda function can take any number of arguments but only one expression, which is evaluated and returned.

Basic Lambda Function
You can use a lambda function in place of a normal function for short tasks.

Example:
# Normal function
def add(x, y):
    return x + y

# Equivalent lambda function
add_lambda = lambda x, y: x + y

# Using the lambda function
result = add_lambda(5, 3)
print(result)  # Output: 8
In this example, both add() and the lambda function perform the same task of adding two numbers.

Lambda with No Arguments
A lambda function can also take no arguments.

Example:
no_args = lambda: "Hello, World!"
print(no_args())  # Output: Hello, World!
Lambda with Conditional Expressions
You can include conditional expressions inside a lambda function.

Example:
max_lambda = lambda x, y: x if x > y else y
print(max_lambda(10, 15))  # Output: 15
This lambda function returns the larger of two values using a conditional expression.

Using Lambdas with Functions like map(), filter(), and reduce()
Lambda functions are commonly used with higher-order functions like map(), filter(), and reduce() to perform operations on sequences such as lists.

Example with map():
The map() function applies a function to each item in an iterable (such as a list) and returns a map object.

numbers = [1, 2, 3, 4]
squares = list(map(lambda x: x ** 2, numbers))
print(squares)  # Output: [1, 4, 9, 16]
Example with filter():
The filter() function filters elements of an iterable based on a condition.

numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6]
Example with reduce():
The reduce() function, which is available in the functools module, applies a function cumulatively to the items in an iterable, reducing them to a single value.


from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 24
Sorting with Lambda Functions
You can use lambda functions as the key argument in sorting functions like sorted() and sort() to specify how the elements should be ordered.

Example:
# List of tuples
points = [(1, 2), (3, 1), (0, -1)]

# Sorting by the second element in each tuple
sorted_points = sorted(points, key=lambda x: x[1])
print(sorted_points)  # Output: [(0, -1), (3, 1), (1, 2)]
In this example, the list of tuples is sorted by the second element of each tuple using a lambda function.

Using Lambdas Inside Functions
Lambda functions can be used as return values or arguments within other functions, making them powerful for writing concise, reusable code.

Example:
def make_multiplier(n):
    return lambda x: x * n

times_3 = make_multiplier(3)
print(times_3(5))  # Output: 15
In this example, make_multiplier() returns a lambda function that multiplies any number by n.

When to Use Lambda Functions
Lambda functions are ideal when:

You need a small function for a short time.
You don’t want to define a function using def for a simple task.
You are using higher-order functions like map(), filter(), or reduce().
However, avoid using lambda functions for complex operations as they can make your code harder to read.

Conclusion
Lambda functions in Python provide a concise way to define small, anonymous functions. They are particularly useful for simple operations and are commonly used with functions like map(), filter(), and reduce(). While they offer flexibility, they should be used judiciously to maintain code readability.


This Markdown file covers Python lambda functions, including their syntax, use cases with functions like `map()`, `filter()`, and `reduce()`, and examples of sorting and conditional expressions. The structure ensures it looks clean and easy to read when previewed on GitHub.





