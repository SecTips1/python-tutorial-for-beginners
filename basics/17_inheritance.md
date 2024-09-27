# 17 Inheritance

## Introduction
Inheritance is a fundamental concept in Object-Oriented Programming (OOP) that allows a class (called a child or subclass) to inherit attributes and methods from another class (called a parent or superclass). Inheritance promotes code reuse and a logical hierarchy between classes.

## Basic Inheritance
To create a subclass, define a new class that inherits from a parent class. The subclass inherits all attributes and methods from the parent, and it can also define its own.

### Example:

```python
# Parent class
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return f"{self.name} makes a sound."

# Child class inheriting from Animal
class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

# Create an instance of Dog
dog = Dog("Buddy")
print(dog.speak())  # Output: Buddy says Woof!
In this example:

The Dog class inherits from the Animal class.
The Dog class overrides the speak() method to provide a specific behavior.
The super() Function
In Python, the super() function allows you to call methods from the parent class inside the child class. This is useful when you want to extend the behavior of the parent class in the child class.

Example:
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Call the parent class's __init__ method
        self.breed = breed

dog = Dog("Buddy", "Golden Retriever")
print(dog.name)  # Output: Buddy
print(dog.breed)  # Output: Golden Retriever
In this case, super() is used to call the __init__() method of the Animal class, which initializes the name attribute in the Dog class.

Method Overriding
A subclass can override methods of its parent class by defining a method with the same name. When you call the method on an instance of the subclass, the subclass's version of the method is executed instead of the parent class's version.

Example:
class Animal:
    def speak(self):
        return "Animal sound"

class Cat(Animal):
    def speak(self):
        return "Meow"

cat = Cat()
print(cat.speak())  # Output: Meow
Here, the Cat class overrides the speak() method from the Animal class to provide its own version.

Multiple Inheritance
Python supports multiple inheritance, meaning a class can inherit from more than one parent class. When using multiple inheritance, the method resolution order (MRO) determines the order in which base classes are searched for methods.

Example:
class Canine:
    def bark(self):
        return "Woof!"

class Pet:
    def play(self):
        return "Plays with owner"

class Dog(Canine, Pet):
    pass

dog = Dog()
print(dog.bark())  # Output: Woof!
print(dog.play())  # Output: Plays with owner
In this example, the Dog class inherits from both Canine and Pet, gaining access to the methods of both classes.

The isinstance() Function
You can use the isinstance() function to check if an object is an instance of a particular class or its subclasses.

Example:
dog = Dog()
print(isinstance(dog, Dog))     # Output: True
print(isinstance(dog, Canine))  # Output: True
print(isinstance(dog, Animal))  # Output: True
Since Dog is a subclass of Canine and Animal, the isinstance() function returns True for all of them.

The issubclass() Function
The issubclass() function checks if a class is a subclass of another class.

Example:
print(issubclass(Dog, Canine))  # Output: True
print(issubclass(Dog, Pet))     # Output: True
print(issubclass(Dog, Animal))  # Output: False
In this case, Dog is a subclass of Canine and Pet, but not Animal.

Inheriting Class Attributes
Class attributes can also be inherited. If a subclass does not define its own class attribute, it will inherit the class attribute from its parent class.

Example:
class Animal:
    species = "Animal"

class Dog(Animal):
    pass

dog = Dog()
print(dog.species)  # Output: Animal
In this case, Dog inherits the class attribute species from Animal.

Polymorphism
Polymorphism allows objects of different classes to be treated as objects of a common superclass. This means you can write code that works with different types of objects in a uniform way.

Example:
class Animal:
    def speak(self):
        return "Animal sound"

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

# Using polymorphism
animals = [Dog(), Cat()]

for animal in animals:
    print(animal.speak())
# Output:
# Woof!
# Meow!
In this example, both Dog and Cat inherit from Animal, and their speak() methods are called based on the type of object, demonstrating polymorphism.

Conclusion
Inheritance is a powerful feature of Object-Oriented Programming that promotes code reuse and logical hierarchy. By understanding how to use inheritance, method overriding, and the super() function, you can write more flexible and maintainable Python code.


This Markdown file covers Python inheritance, including basic inheritance, method overriding, multiple inheritance, and the use of `super()`. It explains how to use `isinstance()`, `issubclass()`, and demonstrates polymorphism with examples. The content is organized clearly and designed to be visually appealing on GitHub.





