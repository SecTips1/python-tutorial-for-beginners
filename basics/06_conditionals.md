# Conditionals in Python
#
# Conditionals allow us to execute certain blocks of code only if specific conditions are met.
# The most commonly used conditional statements in Python are:
# 1. if
# 2. elif (else if)
# 3. else

# 1. if Statement
# The `if` statement executes a block of code if the condition evaluates to True.

x = 10

if x > 5:
    print("x is greater than 5")  # Output: x is greater than 5

# 2. elif Statement
# The `elif` statement checks another condition if the previous `if` or `elif` conditions are False.
# You can chain multiple `elif` conditions.

y = 20

if y > 30:
    print("y is greater than 30")
elif y > 15:
    print("y is greater than 15")  # Output: y is greater than 15
elif y > 10:
    print("y is greater than 10")

# 3. else Statement
# The `else` statement runs if none of the `if` or `elif` conditions are True.

z = 8

if z > 10:
    print("z is greater than 10")
else:
    print("z is 10 or less")  # Output: z is 10 or less

# Nested if Statements
# You can nest `if` statements inside other `if` statements for more complex conditions.

a = 7

if a > 5:
    if a < 10:
        print("a is between 5 and 10")  # Output: a is between 5 and 10

# Conditional Expressions (Ternary Operator)
# Python also supports a shorthand for `if-else` called a conditional expression or ternary operator.

b = 15
result = "Even" if b % 2 == 0 else "Odd"
print(result)  # Output: Odd
