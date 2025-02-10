# Object-Oriented Programming (OOP) in Python

## 📌 Overview
Object-Oriented Programming (OOP) in Python is a programming paradigm that organizes software design around **objects** rather than functions and logic. An object is a **data structure** that contains both **data (attributes)** and **functions (methods)** that operate on the data. OOP makes code **reusable, scalable, and modular**.

---

## 🔑 Key Concepts of OOP

### 🏛 1. Classes and Objects
- **Class**: A blueprint for creating objects (defines attributes & methods).
- **Object**: An instance of a class.

```python
# Defining a Class and Creating an Object
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print("Woof!")

my_dog = Dog("Buddy", 3)
my_dog.bark()  # Output: Woof!
```

### 🔒 2. Encapsulation (Data Hiding)
Encapsulation ensures that an object's data is protected by restricting direct access and allowing modification only through controlled methods.

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance  # Accessor method

account = BankAccount(100)
account.deposit(50)
print(account.get_balance())  # Output: 150
```
- 🔹 Private attributes (__balance) cannot be accessed directly.
- 🔹 Methods (get_balance()) allow controlled access.

### 🏗 3. Inheritance (Code Reusability)
Inheritance allows a class (child class) to reuse properties & methods from another class (parent class).

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass  # Placeholder for derived classes

class Dog(Animal):  # Dog inherits from Animal
    def speak(self):
        return "Woof!"

my_dog = Dog("Buddy")
print(my_dog.speak())  # Output: Woof!
```
- 🔹 Single Inheritance: One class inherits from another.
- 🔹 Multiple Inheritance: A class inherits from multiple parent classes.
- 🔹 Multilevel Inheritance: Inheritance chain (A → B → C).
- 🔹 Hierarchical Inheritance: One parent class, multiple child classes.

### 🔁 4. Polymorphism (Many Forms)
Polymorphism allows the same method name to behave differently in different classes.

```python

class Cat(Animal):
    def speak(self):
        return "Meow!"

animals = [Dog("Buddy"), Cat("Whiskers")]

for animal in animals:
    print(animal.speak())  # Output: Woof! Meow!
```
- 🔹 Method Overriding – Child class redefines a method from the parent class.\n
- 🔹 Method Overloading – Not natively supported in Python but can be simulated using default arguments.

### 🎭 5. Abstraction (Hiding Complexity)
Abstraction hides implementation details and only exposes the necessary features.
```python
from abc import ABC, abstractmethod

class Shape(ABC):  # Abstract Class
    @abstractmethod
    def area(self):
        pass  # Must be implemented in child classes

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

my_circle = Circle(5)
print(my_circle.area())  # Output: 78.5

```
- 🔹 Abstract classes cannot be instantiated.
- 🔹 Forces subclasses to implement the abstract method (area()).


  ###  ✅ Benefits of OOP
  
  ✔Modularity – Code is divided into reusable classes.<br>
        ✔ <strong>Reusability</strong> – Existing classes can be extended to new functionality.<br>
        ✔ <strong>Scalability</strong> – Code can be easily modified or extended.<br>
        ✔ <strong>Security</strong> – Encapsulation restricts unauthorized access.<br>
    </div>

    <h2>🎯 Conclusion</h2>
    <p>Object-Oriented Programming in Python provides a powerful and structured approach to software development. By using <strong>encapsulation, inheritance, polymorphism, and abstraction</strong>, developers can build <em>efficient, maintainable, and scalable</em> applications. 🚀</p>

    <h2>💡 Want to Learn More?</h2>
    <ul>
        <li>📌 <a href="https://docs.python.org/3/tutorial/classes.html" target="_blank">Python OOP Documentation</a></li>
        <li>📌 <a href="https://realpython.com/python3-object-oriented-programming/" target="_blank">Python OOP Tutorial by RealPython</a></li>
    </ul>

    <h2>🛠 Follow Me for More Programming Resources</h2>
    <ul>
        <li>🔗 <a href="https://github.com/Hisham-cse" target="_blank">GitHub: Hisham-cse</a></li>
        <li>🔗 <a href="https://hisham-cse.github.io/Portfolio/" target="_blank">Portfolio: Hisham's Portfolio</a></li>
    </ul>

    <h2>📄 How to Use This in Your GitHub Repository?</h2>
    <ol>
        <li>💻 <strong>Create a new repository</strong> or open an existing one.</li>
        <li>📁 <strong>Add a new file</strong> and name it <code>README.md</code>.</li>
        <li>📋 <strong>Paste the above Markdown content</strong> into the file.</li>
        <li>✅ <strong>Commit and push</strong> the changes to your repository.</li>
    </ol>

    <p>🚀 Now your <strong>GitHub repository</strong> will have a <em>well-structured, professional README file</em> explaining <strong>OOP in Python!</strong></p>

    <div class="footer">
        <a href="https://github.com/Hisham-cse" target="_blank" class="btn">🌟 Follow on GitHub</a>
        <a href="https://hisham-cse.github.io/Portfolio/" target="_blank" class="btn">🔗 Visit Portfolio</a>
    </div>


