# 14 File Handling

## Introduction
File handling is an essential aspect of many programming tasks. Python provides built-in functions and methods to work with files, enabling you to create, read, write, and delete them. The `open()` function is used to open files, and you can perform various operations on them, such as reading from and writing to files.

## Opening a File
To open a file in Python, use the `open()` function, which takes the filename and the mode as arguments. The most common modes are:
- `"r"`: Read (default mode) – opens the file for reading.
- `"w"`: Write – opens the file for writing (creates a new file if it doesn’t exist, or truncates the file if it exists).
- `"a"`: Append – opens the file for appending (creates a new file if it doesn’t exist).
- `"b"`: Binary – opens the file in binary mode (e.g., `"rb"`, `"wb"`).

### Example:

```python
file = open("example.txt", "r")  # Opens the file in read mode
Closing a File
After working with a file, it’s important to close it using the close() method to free up system resources.

python
Copy code
file.close()
Writing to a File
To write to a file, you can open it in "w" (write) or "a" (append) mode. In write mode, the file is overwritten if it exists, while append mode adds data to the end of the file.

python
Copy code
# Writing to a file
file = open("example.txt", "w")
file.write("Hello, World!\n")
file.write("This is a new line.")
file.close()
Using with for File Handling
A safer and more Pythonic way to handle files is by using a with statement. It ensures that the file is properly closed after the block is executed, even if an exception occurs.

python
Copy code
with open("example.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new line.")
Reading from a File
To read the contents of a file, open it in "r" (read) mode and use one of the following methods:

read(): Reads the entire content of the file.
readline(): Reads one line at a time.
readlines(): Reads all lines into a list.
Example:
python
Copy code
# Reading the entire file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
python
Copy code
# Reading line by line
with open("example.txt", "r") as file:
    line = file.readline()
    while line:
        print(line, end="")  # end="" prevents adding an extra newline
        line = file.readline()
python
Copy code
# Reading all lines into a list
with open("example.txt", "r") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())  # strip() removes extra whitespace and newlines
Appending to a File
To append content to an existing file, open it in "a" (append) mode. This will add the new content to the end of the file without overwriting the existing data.

python
Copy code
with open("example.txt", "a") as file:
    file.write("\nAppending this line to the file.")
Working with Binary Files
In addition to text files, you can work with binary files (e.g., images, audio files) by opening them in binary mode ("rb", "wb", or "ab").

python
Copy code
# Writing to a binary file
with open("image.jpg", "wb") as file:
    file.write(b"\x89PNG\r\n\x1a\n")  # Writing binary data
Checking if a File Exists
Before performing file operations, it’s often useful to check if a file exists to avoid errors. You can use the os module for this.

python
Copy code
import os

if os.path.exists("example.txt"):
    print("File exists.")
else:
    print("File does not exist.")
Deleting a File
You can delete a file using the remove() function from the os module.

python
Copy code
import os

if os.path.exists("example.txt"):
    os.remove("example.txt")
    print("File deleted.")
else:
    print("File does not exist.")
Conclusion
File handling in Python is simple and flexible, allowing you to work with text and binary files efficiently. By using the open() function and handling files with the with statement, you can ensure that resources are properly managed. Mastering file handling is crucial for many programming tasks, including data storage, logging, and configuration management.

vbnet
Copy code

This Markdown file explains Python file handling, including reading, writing, appending, working with binary files, and deleting files. The content is structured to look visually nice when previewed in GitHub, with clear sections and code examples.





