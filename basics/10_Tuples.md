# 10 Tuples

## Introduction
A tuple is a collection of items that is ordered and unchangeable (immutable). Tuples are similar to lists, but unlike lists, once a tuple is created, you cannot modify, add, or remove items from it. Tuples are defined using parentheses `()`.

Tuples are useful when you want to create a collection of items that should not change throughout the program.

## Creating a Tuple. You can create a tuple by placing a sequence of items separated by commas inside parentheses `()`.

# Example of a tuple
my_tuple = (1, 2, 3, 4, 5)

# Tuple with mixed data types
mixed_tuple = (1, "Hello", 3.14, False)


## Tuple Without Parentheses. You can also create a tuple without parentheses by simply separating the items with commas. This is known as "tuple packing."

my_tuple = 1, 2, 3
Single-Item Tuple
To define a tuple with a single element, you need to add a trailing comma. Without the comma, Python treats it as a regular variable or expression.

# Single item tuple
single_tuple = (5,)
Accessing Tuple Elements
You can access elements in a tuple just like you would in a list, using indexing. The first item has an index of 0.

# Accessing the first element
print(my_tuple[0])  # Output: 1

# Accessing the last element
print(my_tuple[-1])  # Output: 5
Negative Indexing
You can also use negative indexing to access items from the end of the tuple.

# Accessing the second last element
print(my_tuple[-2])  # Output: 4
Tuple Operations

## Tuple Length. You can find the number of elements in a tuple using the len() function.

print(len(my_tuple))  # Output: 5
Concatenation
You can concatenate two or more tuples using the + operator.

tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
concatenated_tuple = tuple1 + tuple2
print(concatenated_tuple)  # Output: (1, 2, 3, 4, 5, 6)


## Repeating Tuples. You can repeat a tuple a specified number of times using the * operator.

repeated_tuple = my_tuple * 2
print(repeated_tuple)  # Output: (1, 2, 3, 4, 5, 1, 2, 3, 4, 5)

## Tuple Immutability. Tuples are immutable, meaning you cannot modify, add, or remove items after the tuple has been created.

# This will raise an error
my_tuple[0] = 10  # TypeError: 'tuple' object does not support item assignment
If you need a tuple that can be changed, you will have to convert it into a list first.

# Convert tuple to list, modify, then convert back to tuple
my_list = list(my_tuple)
my_list[0] = 10
my_tuple = tuple(my_list)
print(my_tuple)  # Output: (10, 2, 3, 4, 5)


## Iterating Over a Tuple. You can loop through a tuple just like you would with a list.

for item in my_tuple:
    print(item)


## Unpacking Tuples
You can unpack a tuple into individual variables. The number of variables must match the number of elements in the tuple.

a, b, c, d, e = my_tuple
print(a)  # Output: 1
print(e)  # Output: 5


## Using the * Operator for Unpacking
If you do not know the exact number of elements in a tuple, you can use the * operator to assign the remaining values to a list.

a, b, *rest = my_tuple
print(a)     # Output: 1
print(b)     # Output: 2
print(rest)  # Output: [3, 4, 5]

## When to Use Tuples
Tuples are useful in situations where you want to ensure that the data cannot be modified. Common use cases include:

Returning multiple values from a function
Grouping related but distinct items
Working with constant data
Conclusion
Tuples are similar to lists, but they are immutable and generally used for storing fixed collections of items. Understanding when to use tuples vs. lists is an important aspect of efficient Python programming.

css
Copy code

This Markdown file covers tuples, their creation, basic operations, and examples in a clear and structured manner for GitHub documentation.





