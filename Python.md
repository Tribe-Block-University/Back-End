# Python Tutorial 🐍

Python is a high-level, interpreted programming language known for its simplicity and readability. It is widely used for web development, data science, artificial intelligence, automation, and more.

## 📚 Topics Covered
1. [Introduction to Python](#introduction-to-python)
2. [Setting Up Python](#setting-up-python)
3. [Variables & Data Types](#variables--data-types)
4. [Control Flow](#control-flow)
5. [Functions & Modules](#functions--modules)
6. [Object-Oriented Programming](#object-oriented-programming)
7. [File Handling](#file-handling)
8. [Working with Databases](#working-with-databases)
9. [Web Development with Flask & Django](#web-development-with-flask--django)
10. [Error Handling](#error-handling)

---

## 1. Introduction to Python  
Python is an interpreted language, meaning it runs line by line. It is widely used in various fields including web development, AI, and automation.

```python
print("Hello, Python!")
```
# Setting Up Python
Installing Python
* Download from [Python.org](https://www.python.org/downloads/)
* Verify installation using:
```sh
python --version
```

# Variables & Data Types
Python supports multiple data types:
```python
name = "Alice"  # String
age = 25  # Integer
pi = 3.14  # Float
is_active = True  # Boolean
```

# Control Flow
## If-Else Condition
```python
if age > 18:
    print("Adult")
else:
    print("Minor")
```

## Loops
```python
for i in range(5):
    print(i)
```

# Functions & Modules
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))
```

# Object-Oriented Programming
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hi, I'm {self.name}!"

p1 = Person("Alice", 25)
print(p1.greet())
```

# File Handling
```python
with open("file.txt", "w") as f:
    f.write("Hello, File!")
```

# Working with Databases
```python
import sqlite3
conn = sqlite3.connect("database.db")
cursor = conn.cursor()
cursor.execute("CREATE TABLE users (id INTEGER, name TEXT)")
conn.commit()
```

# Web Development with Flask & Django
Flask Example:
```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def home():
    return "Welcome to Flask!"

if __name__ == "__main__":
    app.run(debug=True)
```

# Error Handling
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

🌐 Further Reading
* [Python Official Docs](https://docs.python.org/3/)
* [W3Schools Python](https://www.w3schools.com/python/)

