<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OOP in Python</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
        }
        .section-title {
            font-size: 1.5em;
            font-weight: bold;
            margin-top: 20px;
        }
        .subsection-title {
            font-size: 1.25em;
            font-weight: bold;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <h1>Object-Oriented Programming (OOP) in Python</h1>

    <div class="section-title">Overview</div>
    <p>
        Object-Oriented Programming (OOP) in Python is a programming paradigm that organizes software design around data, or objects, rather than functions and logic. An object is a data structure that contains data (attributes) and functions (methods) that operate on the data. OOP allows for the creation of reusable and modular code by encapsulating data and behavior within objects.
    </p>

    <div class="section-title">Key Concepts</div>

    <div class="subsection-title">1. Classes and Objects</div>
    <p>
        <strong>Class</strong>: A blueprint for creating objects. It defines the attributes and methods that the objects created from the class will have.
    </p>
    <p>
        <strong>Object</strong>: An instance of a class. It is created using the class definition and can have its own state and behavior.
    </p>
    <pre><code class="language-python">
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print("Woof!")

my_dog = Dog("Buddy", 3)
my_dog.bark()  # Output: Woof!
    </code></pre>

    <div class="subsection-title">2. Encapsulation</div>
    <p>
        Encapsulation is the concept of bundling data (attributes) and methods (functions) that operate on the data within a single unit, or class. It helps to protect the data from unauthorized access and modification.
    </p>
    <pre><code class="language-python">
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(100)
account.deposit(50)
print(account.get_balance())  # Output: 150
    </code></pre>

    <div class="subsection-title">3. Inheritance</div>
    <p>
        Inheritance allows a class to inherit attributes and methods from another class, promoting code reusability. The class that inherits is called the subclass, and the class being inherited from is called the superclass.
    </p>
    <pre><code class="language-python">
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

my_dog = Dog("Buddy")
print(my_dog.speak())  # Output: Woof!
    </code></pre>

    <div class="subsection-title">4. Polymorphism</div>
    <p>
        Polymorphism allows different classes to be treated as instances of the same class through inheritance. It enables a single interface to represent different underlying forms (data types).
    </p>
    <pre><code class="language-python">
class Cat(Animal):
    def speak(self):
        return "Meow!"

animals = [Dog("Buddy"), Cat("Whiskers")]
for animal in animals:
    print(animal.speak())  # Output: Woof! Meow!
    </code></pre>

    <div class="subsection-title">5. Abstraction</div>
    <p>
        Abstraction is the process of hiding the implementation details and showing only the essential features of an object. It allows the user to interact with the object without knowing the internal workings.
    </p>
    <pre><code class="language-python">
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

my_circle = Circle(5)
print(my_circle.area())  # Output: 78.5
    </code></pre>

    <div class="section-title">Benefits of OOP</div>
    <ul>
        <li><strong>Modularity</strong>: Code can be divided into reusable classes.</li>
        <li><strong>Reusability</strong>: Existing classes can be reused to create new classes.</li>
        <li><strong>Scalability</strong>: Easy to manage and expand codebase.</li>
        <li><strong>Maintainability</strong>: Encapsulation and modularity make the code easier to maintain and understand.</li>
    </ul>

    <div class="section-title">Conclusion</div>
    <p>
        Object-Oriented Programming in Python provides a powerful and flexible way to write clean, modular, and reusable code. By using classes and objects, encapsulation, inheritance, polymorphism, and abstraction, developers can create sophisticated and maintainable applications.
    </p>
</body>
</html>
