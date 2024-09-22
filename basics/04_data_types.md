# Data Types in Python

# In Python, every value is associated with a data type, which determines the type of operations
# that can be performed on the value and how it is stored in memory.

# 1. Numeric Types:
# - int: Represents whole numbers (e.g., 5, 100, -10)
# - float: Represents decimal numbers (e.g., 5.0, 3.14, -0.001)
# - complex: Represents complex numbers with real and imaginary parts (e.g., 2 + 3j)

x = 10        # int
y = 3.14      # float
z = 1 + 2j    # complex

# 2. Sequence Types:
# - str: String, a sequence of characters (e.g., 'Hello', "Python")
# - list: An ordered collection of items that can be of different types (e.g., [1, 2, 'three'])
# - tuple: Similar to a list, but immutable (e.g., (1, 2, 'three'))

s = "Hello, Python"  # str
my_list = [1, 2, 3]  # list
my_tuple = (1, 2, 3) # tuple

# 3. Boolean Type:
# - bool: Represents logical values True or False

is_python_fun = True   # bool
is_raining = False     # bool

# 4. Mapping Type:
# - dict: A collection of key-value pairs (e.g., {"name": "John", "age": 25})

my_dict = {"name": "Alice", "age": 30}

# 5. Set Types:
# - set: An unordered collection of unique elements (e.g., {1, 2, 3})
# - frozenset: Similar to a set, but immutable

my_set = {1, 2, 3}               # set
frozen_set = frozenset([1, 2, 3]) # frozenset

# Type Conversion:
# Python allows conversion between different data types using functions like int(), float(), str(), etc.

x = 10         # int
y = str(x)     # Convert int to string
z = float(x)   # Convert int to float

# Checking Data Types:
# You can use the type() function to check the data type of a variable.

x = 10
print(type(x))  # Output: <class 'int'>
