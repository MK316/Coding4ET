🔍[BACK to the Main page](https://github.com/MK316/Coding4ET/blob/main/README.md)

# Lesson 4 Data types

Python has several built-in data types that are commonly used. Here's a brief overview of each. Note that we will be focusing on some of the data types listed below for our purpose.

* **Number:** integers, floating numbers
* **String: "a book", "1.23", "KL234", 'an apple', 'A cat chases a mouse.', etc**
* **List:** [1, 2, 4, 8], ["apple","banana","melon"], ["1","apple","2","banana"], etc.
* **Dictionary:** {'Subject': 'Mary', 'Object': "cakes", 'Verb': 'bought'}, {"ID": 20240235, 'Name': 'Mary'}, etc.
* **Tuple:** e.g., months = ("January", "February","March", ....)

---
### 1. Number
+ Integers (**int**): Whole numbers like 3, 100, -1.
+ Floating-point numbers (**float**): Numbers with a decimal point like 2.3, -0.1, 3.14.
+ Complex numbers (complex): Numbers with a real and imaginary part, e.g., 3 + 4j.


🌀***Example***

Numbers in Python can be integers (whole numbers) or floats (numbers with decimal points).

**Integer:**
```
# An example of an integer
age = 25
print("Age:", age)
```

**Float:**

```
# An example of a float
average_score = 82.5
print("Average Score:", average_score)
```

---
### 2. String (str):
Textual data enclosed in single ('text'), double ("text"), or triple quotes ('''text is ...''' or """text is ..."""). For example, "Hello", 'Python'.

🌀***Example***

Strings are sequences of characters and are used to store text.

```
# An example of a string
name = input()  # A pop-up box will appear and wait for your input. Type a name.
print("Hello, %s!"%name)  # % operator: The % operator is used for string formatting. It links the string "Hello, %s!" with the variable name to replace the %s placeholder.
```

Or you can use Python's f-string for string formatting (from Python 3.6; same result)

+ Note: The currently Colab uses higher than Python 3.6, so you can use this f-string operator.

```
# An example of a string
name = input()  # A pop-up box will appear and wait for your input. Type a name.
print(f"Hello, {name}!)    # 
```

```
mytext = """
Long long time ago, there lived a lion called Lezzi.
One day, ....
"""
print(mytext)
```
> Long long time ago, there lived a lion called Lezzi.
One day, ....

---
### 3. List (list):
An ordered, mutable (changeable) collection of items. Lists are defined with square brackets, e.g., [1, 2, 3] or ['apple', 'banana', 'cherry'].

🌀***Example***

```
# An example of a list
favorite_books = ["To Kill a Mockingbird", "1984", "The Great Gatsby"]
print("Favorite Books:", favorite_books)
```

---
### 4. Dictionary (dict):
A collection of key-value pairs. Dictionaries are defined with curly braces containing key-value pairs separated by colons, e.g., {'name': 'Alice', 'age': 25}.

🌀***Example***
```
# An example of a dictionary
student_grades = {"Alice": 90, "Bob": 85, "Charlie": 95}
print("Student Grades:", student_grades)
```

```
# Return Alice's grade
student_grades['Alice']
```

---
### 5. Tuple (tuple): 
An ordered, immutable collection of items. Tuples are defined with parentheses, e.g., (1, 2, 3) or ('a', 'b', 'c').

🌀***Example***

```
# An example of a tuple
months_of_the_year = ("January", "February", "March", "April")
print("Months of the Year:", months_of_the_year)
```
---
### 6. Boolean (bool): 
Represents truth values. The two boolean values are True and False.


### 7. Set (set):
An unordered collection of unique items. Sets are defined with curly braces, e.g., {1, 2, 3} or {'apple', 'banana', 'cherry'}. Note that sets do not allow duplicate elements.

### 8. NoneType (None): 
A special type representing the absence of a value or a null value.

Each data type serves a specific purpose and can be used in different scenarios in Python programming. For instance, lists and tuples are great for storing ordered collections of items, dictionaries are ideal for storing related data as key-value pairs, and sets are useful for storing unique items and performing set operations.


[🔝](#Lesson-4-Data-types)

🔍[BACK to the Main page](https://github.com/MK316/Coding4ET/blob/main/README.md)
