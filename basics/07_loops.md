# Loops in Python
#
# Loops allow you to repeatedly execute a block of code as long as a condition is true.
# Python supports two types of loops:
# 1. for loop
# 2. while loop

# 1. for Loop
# A `for` loop is used to iterate over a sequence (like a list, tuple, dictionary, string, or range).

# Example: Iterating over a list
numbers = [1, 2, 3, 4, 5]

for num in numbers:
    print(num)  # Output: 1 2 3 4 5 (each number on a new line)

# Example: Using `range()`
# The `range()` function generates a sequence of numbers.
for i in range(5):
    print(i)  # Output: 0 1 2 3 4

# 2. while Loop
# A `while` loop repeats as long as the condition is True.

x = 0

while x < 5:
    print(x)  # Output: 0 1 2 3 4
    x += 1  # Increment x

# 3. Loop Control Statements
# Python provides three keywords to control loop execution:
# - break: Exits the loop completely.
# - continue: Skips the rest of the current iteration and moves to the next iteration.
# - pass: Does nothing, acts as a placeholder.

# Example: break
for i in range(10):
    if i == 5:
        break  # Loop will stop when i is 5
    print(i)  # Output: 0 1 2 3 4

# Example: continue
for i in range(5):
    if i == 2:
        continue  # Skips printing when i is 2
    print(i)  # Output: 0 1 3 4

# Example: pass
for i in range(3):
    pass  # Does nothing, just a placeholder for future code

# Nested Loops
# You can have loops inside other loops (nested loops).

for i in range(3):
    for j in range(2):
        print(f"i = {i}, j = {j}")
        # Output:
        # i = 0, j = 0
        # i = 0, j = 1
        # i = 1, j = 0
        # i = 1, j = 1
        # i = 2, j = 0
        # i = 2, j = 1
