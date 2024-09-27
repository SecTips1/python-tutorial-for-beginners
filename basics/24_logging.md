# 24 Logging

## Introduction
Logging is a vital aspect of debugging and monitoring applications in production environments. Python's `logging` module provides a flexible framework for adding logging to your applications. It allows you to track events, log error messages, warnings, or informational messages, and log those events to different outputs like console or files.

### Why Use Logging:
- **Track application behavior**: Log key events to understand the flow of your program.
- **Debugging**: Record error messages, stack traces, and other details to diagnose problems.
- **Monitor applications**: Use logging to capture important events while the program is running in production.

## Basic Logging Setup
You can quickly get started with logging using the basic configuration provided by Python’s `logging` module.

### Example:
```python
import logging

# Set up basic configuration for logging
logging.basicConfig(level=logging.DEBUG)

logging.debug("This is a debug message")
logging.info("This is an info message")
logging.warning("This is a warning message")
logging.error("This is an error message")
logging.critical("This is a critical message")
Output:
vbnet
Copy code
DEBUG:root:This is a debug message
INFO:root:This is an info message
WARNING:root:This is a warning message
ERROR:root:This is an error message
CRITICAL:root:This is a critical message
Logging Levels
Python's logging module has five standard levels indicating the severity of events:

DEBUG: Detailed information for diagnosing problems.
INFO: Confirmation that things are working as expected.
WARNING: Indication that something unexpected happened or may happen.
ERROR: A more serious problem that has occurred.
CRITICAL: A very serious error, indicating that the program may not be able to continue running.
The default level is WARNING, meaning that only messages at this level or higher (ERROR, CRITICAL) are logged unless you configure it otherwise.

Customizing Logging Output
You can customize the format of the log messages using the format argument in basicConfig().

Example:
python
Copy code
logging.basicConfig(level=logging.INFO, format='%(asctime)s - %(levelname)s - %(message)s')

logging.info("Application started")
Output:
mathematica
Copy code
2024-09-30 12:00:00,123 - INFO - Application started
This format includes the timestamp, the severity level, and the actual log message.

Logging to a File
You can direct the log output to a file by setting the filename parameter in basicConfig().

Example:
python
Copy code
logging.basicConfig(filename='app.log', level=logging.ERROR, format='%(asctime)s - %(levelname)s - %(message)s')

logging.error("This error will be logged to a file")
This will log messages with level ERROR or higher to app.log.

Creating Loggers
The logging module allows you to create loggers for different parts of your application. A logger object is created using the getLogger() function, which allows you to organize your logging by components.

Example:
python
Copy code
logger = logging.getLogger('my_logger')
logger.setLevel(logging.DEBUG)

logger.debug("This is a debug message from my_logger")
By using different loggers, you can easily separate logging for different components of your application.

Handlers in Logging
Handlers allow you to route log messages to different destinations, such as console, files, or remote servers. You can attach multiple handlers to a single logger to send the log messages to various outputs.

Example: Logging to Console and File
python
Copy code
# Create logger
logger = logging.getLogger('example_logger')
logger.setLevel(logging.DEBUG)

# Create a console handler
console_handler = logging.StreamHandler()
console_handler.setLevel(logging.DEBUG)

# Create a file handler
file_handler = logging.FileHandler('example.log')
file_handler.setLevel(logging.ERROR)

# Create a formatter and set it for the handlers
formatter = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')
console_handler.setFormatter(formatter)
file_handler.setFormatter(formatter)

# Add the handlers to the logger
logger.addHandler(console_handler)
logger.addHandler(file_handler)

# Log some messages
logger.debug("This is a debug message")
logger.error("This error will be logged to both console and file")
In this example:

Debug messages are sent to the console.
Error messages are sent to both the console and the example.log file.
Logging Exceptions
You can log exceptions with the exception() method, which automatically captures and logs the exception traceback.

Example:
python
Copy code
try:
    1 / 0
except ZeroDivisionError:
    logging.exception("An exception occurred")
Output:
vbnet
Copy code
ERROR:root:An exception occurred
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
This captures the full traceback of the exception in the log.

Rotating Log Files
For applications that run for long periods of time, it’s common to rotate log files to avoid creating a massive log file. The logging.handlers module provides a RotatingFileHandler for this purpose.

Example: Using RotatingFileHandler
python
Copy code
from logging.handlers import RotatingFileHandler

# Set up a rotating file handler
handler = RotatingFileHandler("app.log", maxBytes=2000, backupCount=5)
logging.basicConfig(handlers=[handler], level=logging.INFO, format='%(asctime)s - %(message)s')

for i in range(100):
    logging.info(f"Log entry {i}")
maxBytes: The maximum size of the log file before rotation.
backupCount: The number of backup files to keep.
Best Practices for Logging
Use appropriate log levels: Only use DEBUG for development, and use ERROR or CRITICAL for logging critical issues in production.
Avoid excessive logging: Too many log entries can clutter logs and make it harder to find useful information.
Log exceptions properly: Always use logging.exception() to capture the full traceback when logging exceptions.
Use rotating log files: In long-running applications, use log rotation to prevent log files from growing indefinitely.
Organize loggers by modules: Use different loggers for different modules or components of your application to keep logs clean and organized.
Conclusion
Logging is an essential tool for debugging and monitoring applications. Python’s logging module offers a flexible and easy-to-use way to handle logging, whether it’s to the console, files, or other handlers. By using loggers, handlers, and formatters, you can set up effective logging systems for both small scripts and large-scale applications.

vbnet
Copy code

This Markdown file explains how to use Python’s `logging` module, covering topics such as basic logging, creating loggers, handlers, logging exceptions, and using rotating log files. The structure ensures that it’s easy to read and visually appealing when previewed on GitHub.





