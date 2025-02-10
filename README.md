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
