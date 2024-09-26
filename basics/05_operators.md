# Operators in Python
# 
# Operators are special symbols that perform specific operations on variables and values.
# Python supports several types of operators:
# 1. Arithmetic Operators
# 2. Comparison Operators
# 3. Logical Operators
# 4. Assignment Operators
# 5. Bitwise Operators

# 1. Arithmetic Operators
# These operators are used to perform mathematical operations.
# + : Addition
# - : Subtraction
# * : Multiplication
# / : Division
# % : Modulus (remainder)
# ** : Exponentiation (power)
# // : Floor division (quotient without remainder)

a = 10
b = 3

add = a + b        # 13
subtract = a - b   # 7
multiply = a * b   # 30
divide = a / b     # 3.333...
modulus = a % b    # 1
exponent = a ** b  # 1000
floor_div = a // b # 3

# 2. Comparison Operators
# Used to compare two values, and the result is either True or False.
# == : Equal to
# != : Not equal to
# >  : Greater than
# <  : Less than
# >= : Greater than or equal to
# <= : Less than or equal to

x = 5
y = 10

equal = (x == y)     # False
not_equal = (x != y) # True
greater = (x > y)    # False
less = (x < y)       # True
greater_equal = (x >= y)  # False
less_equal = (x <= y)     # True

# 3. Logical Operators
# Used to combine conditional statements.
# and : True if both operands are True
# or  : True if at least one operand is True
# not : Inverts the boolean value

condition1 = (x < y)   # True
condition2 = (x > 2)   # True

logical_and = condition1 and condition2  # True
logical_or = condition1 or condition2    # True
logical_not = not condition1             # False

# 4. Assignment Operators
# Used to assign values to variables.
# =  : Simple assignment
# += : Add and assign
# -= : Subtract and assign
# *= : Multiply and assign
# /= : Divide and assign
# %= : Modulus and assign
# **= : Exponent and assign
# //= : Floor divide and assign

z = 10
z += 5  # z = z + 5 -> 15
z *= 2  # z = z * 2 -> 30

# 5. Bitwise Operators
# Operators used to work with binary numbers.
# &  : AND
# |  : OR
# ^  : XOR
# ~  : NOT
# << : Left shift
# >> : Right shift

m = 5  # binary: 0101
n = 3  # binary: 0011

bitwise_and = m & n    # 1  -> binary: 0001
bitwise_or = m | n     # 7  -> binary: 0111
bitwise_xor = m ^ n    # 6  -> binary: 0110
bitwise_not = ~m       # -6 -> binary: 1010 (two's complement)
left_shift = m << 1    # 10 -> binary: 1010
right_shift = m >> 1   # 2  -> binary: 0010
