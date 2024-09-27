# 16 Classes

## Introduction
A class in Python is a blueprint for creating objects. Classes allow you to bundle data (attributes) and functionality (methods) together. Python supports Object-Oriented Programming (OOP), which uses the concept of classes and objects to organize code in a more modular and reusable way.

## Defining a Class
To define a class, use the `class` keyword followed by the class name.

### Example:

```python
class Dog:
    # Class attribute
    species = "Canis familiaris"

    # Initializer method (constructor)
    def __init__(self, name, age):
        # Instance attributes
        self.name = name
        self.age = age

    # Instance method
    def bark(self):
        return f"{self.name} says Woof!"
In this example:

species is a class attribute (shared by all instances).
name and age are instance attributes (unique to each instance).
bark() is an instance method that returns a string when called.
Creating an Object
To create an object (an instance of a class), you call the class as if it were a function.

Example:
dog1 = Dog("Buddy", 3)
dog2 = Dog("Max", 5)

print(dog1.name)  # Output: Buddy
print(dog2.bark())  # Output: Max says Woof!
Here, dog1 and dog2 are instances of the Dog class, each with its own attributes and behavior.

The __init__() Method (Constructor)
The __init__() method is a special method in Python classes. It is called when a new object is instantiated, and it is used to initialize the object's attributes.

Example:
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person = Person("Alice", 30)
print(person.name)  # Output: Alice
Instance vs Class Attributes
Instance attributes are unique to each object.
Class attributes are shared across all instances of the class.
Example:
class Car:
    wheels = 4  # Class attribute

    def __init__(self, brand):
        self.brand = brand  # Instance attribute

car1 = Car("Toyota")
car2 = Car("Honda")

print(car1.wheels)  # Output: 4
print(car2.wheels)  # Output: 4
print(car1.brand)  # Output: Toyota
print(car2.brand)  # Output: Honda
In this case, wheels is a class attribute (shared), while brand is an instance attribute (unique to each car).

Methods
Methods are functions that belong to a class and can operate on instance data. You can define both instance methods (which work on a specific object) and class methods (which work on class-level data).

Example of Instance Method:
class Cat:
    def __init__(self, name, color):
        self.name = name
        self.color = color

    def meow(self):
        return f"{self.name} says Meow!"

cat = Cat("Whiskers", "gray")
print(cat.meow())  # Output: Whiskers says Meow!
Class Methods
Class methods can modify a class's state that applies across all instances. Use the @classmethod decorator to define a class method. Class methods take cls as the first parameter, which refers to the class itself.

Example:
class Animal:
    species = "Mammal"

    @classmethod
    def change_species(cls, new_species):
        cls.species = new_species

Animal.change_species("Bird")
print(Animal.species)  # Output: Bird
Static Methods
Static methods do not modify class or instance states. They are like regular functions but belong to the class's namespace. Use the @staticmethod decorator to define a static method.

Example:
class MathOperations:
    @staticmethod
    def add(x, y):
        return x + y

result = MathOperations.add(5, 3)
print(result)  # Output: 8
Inheritance
Inheritance allows a class (child class) to inherit the attributes and methods of another class (parent class). This promotes code reuse and a hierarchical structure.

Example:
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        raise NotImplementedError("Subclass must implement abstract method")

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

dog = Dog("Buddy")
cat = Cat("Whiskers")

print(dog.speak())  # Output: Buddy says Woof!
print(cat.speak())  # Output: Whiskers says Meow!
In this example, Dog and Cat classes inherit from the Animal class, and each provides its own implementation of the speak() method.

The super() Function
The super() function allows you to call methods from the parent class inside a child class. It is commonly used to extend the behavior of the parent class.

Example:
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

class Car(Vehicle):
    def __init__(self, brand, model):
        super().__init__(brand)
        self.model = model

car = Car("Toyota", "Corolla")
print(car.brand)  # Output: Toyota
print(car.model)  # Output: Corolla
Conclusion
Classes are a powerful feature of Python that enable Object-Oriented Programming. Understanding how to define classes, create objects, and use inheritance can help you write more organized and reusable code. By structuring your code around objects and classes, you can build more complex programs in a manageable way.


This Markdown file introduces Python classes, covering topics like defining classes, creating objects, using methods, inheritance, and the `super()` function. The content is organized to be visually appealing and clear when previewed on GitHub, with well-structured code examples for each concept.





