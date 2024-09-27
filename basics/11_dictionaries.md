# 11 Dictionaries

## Introduction
In Python, a dictionary is a collection of key-value pairs. Each key in a dictionary is unique, and it is used to access its corresponding value. Dictionaries are unordered, mutable, and indexed by keys, not by a sequence of numbers like lists or tuples. Dictionaries are defined using curly braces `{}` with key-value pairs separated by colons `:`.

## Creating a Dictionary
You can create a dictionary by placing key-value pairs inside curly braces `{}`.

# Example of a dictionary
my_dict = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

## Creating an Empty Dictionary
An empty dictionary can be created using empty curly braces or the dict() function.

empty_dict = {}
another_empty_dict = dict()

## Accessing Dictionary Items
You can access dictionary values by referring to their keys.

# Accessing the value associated with a key
print(my_dict["name"])  # Output: John
You can also use the get() method to access the value, which returns None if the key does not exist, rather than raising an error.

print(my_dict.get("age"))  # Output: 30
print(my_dict.get("address"))  # Output: None


## Modifying a Dictionary
Dictionaries are mutable, so you can add, update, or remove key-value pairs after the dictionary has been created.

Adding or Updating Items
You can add new key-value pairs or update the value of an existing key.

# Adding a new key-value pair
my_dict["email"] = "john@example.com"

# Updating the value of an existing key
my_dict["age"] = 31
print(my_dict)  
# Output: {'name': 'John', 'age': 31, 'city': 'New York', 'email': 'john@example.com'}


## Removing Items. You can remove key-value pairs using the pop(), del, or popitem() methods.

pop(): Removes the item with the specified key.
del: Deletes the item with the specified key or the entire dictionary.
popitem(): Removes the last inserted key-value pair.

# Removing an item using pop()
my_dict.pop("city")  # Output: 'New York'

# Removing an item using del
del my_dict["email"]

# Removing the last inserted key-value pair
my_dict.popitem()  # Output: ('age', 31)

# Deleting the entire dictionary
# del my_dict

# Dictionary Methods. Dictionaries come with several useful methods:

keys(), values(), and items()
keys(): Returns a view object of all keys in the dictionary.
values(): Returns a view object of all values in the dictionary.
items(): Returns a view object of all key-value pairs (as tuples).

# Getting all keys
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])

# Getting all values
print(my_dict.values())  # Output: dict_values(['John', 31])

# Getting all key-value pairs
print(my_dict.items())  # Output: dict_items([('name', 'John'), ('age', 31)])
update()
The update() method updates the dictionary with the key-value pairs from another dictionary or from key-value pairs provided as arguments.

my_dict.update({"age": 32, "city": "Boston"})
print(my_dict)  

# Output: {'name': 'John', 'age': 32, 'city': 'Boston'}
Iterating Over a Dictionary
You can loop through the keys, values, or key-value pairs in a dictionary.

# Looping through keys
for key in my_dict:
    print(key)

# Looping through values
for value in my_dict.values():
    print(value)

# Looping through key-value pairs
for key, value in my_dict.items():
    print(f"{key}: {value}")
Dictionary Comprehensions
Similar to list comprehensions, you can create dictionaries using dictionary comprehensions.

# Example: Creating a dictionary with squares of numbers
squares = {x: x**2 for x in range(1, 6)}
print(squares)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

## Checking for Key Existence
You can check if a key exists in a dictionary using the in keyword.

if "name" in my_dict:
    print("Key 'name' exists in the dictionary")
Nested Dictionaries
A dictionary can contain another dictionary, allowing you to store nested data structures.

python
Copy code
nested_dict = {
    "person1": {"name": "Alice", "age": 25},
    "person2": {"name": "Bob", "age": 30}
}

# Accessing nested dictionary values
print(nested_dict["person1"]["name"])  # Output: Alice
When to Use Dictionaries
Dictionaries are ideal when you need to associate pairs of related data, such as mapping user names to email addresses, storing configuration options, or working with JSON-like data.

Conclusion
Dictionaries are an essential Python data structure for storing and managing data in key-value pairs. With their flexibility and efficient lookups, dictionaries are widely used in a variety of applications.

css
Copy code

This Markdown file covers the basics of dictionaries, their operations, methods, and examples in a structured and easy-to-understand format suitable for GitHub documentation.





