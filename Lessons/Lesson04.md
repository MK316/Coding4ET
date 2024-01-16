# Lesson 4 Data types

Python has several built-in data types that are commonly used. Here's a brief overview of each. However, note that we will be focusing on the data types listed below for our purpose.

* Number
* String
* List
* Dictionary
* Tuple


### 1. Number
+ Integers (**int**): Whole numbers like 3, 100, -1.
+ Floating-point numbers (**float**): Numbers with a decimal point like 2.3, -0.1, 3.14.
+ Complex numbers (complex): Numbers with a real and imaginary part, e.g., 3 + 4j.


🌀**_Example_**

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


### 2. String (str):
Textual data enclosed in single ('...'), double ("..."), or triple quotes ('''...''' or """..."""). For example, "Hello", 'Python'.

🌀**_Example_**

Strings are sequences of characters and are used to store text.

```
# An example of a string
name = input()
print("Hello, %s!"%name)
```

### 3. List (list):
An ordered, mutable (changeable) collection of items. Lists are defined with square brackets, e.g., [1, 2, 3] or ['apple', 'banana', 'cherry'].

🌀**_Example_**

```
# An example of a list
favorite_books = ["To Kill a Mockingbird", "1984", "The Great Gatsby"]
print("Favorite Books:", favorite_books)
```


### 4. Dictionary (dict):
A collection of key-value pairs. Dictionaries are defined with curly braces containing key-value pairs separated by colons, e.g., {'name': 'Alice', 'age': 25}.

🌀**_Example_**
```
# An example of a dictionary
student_grades = {"Alice": 90, "Bob": 85, "Charlie": 95}
print("Student Grades:", student_grades)
```

```
# Return Alice's grade
student_grades['Alice']
```

### 5. Tuple (tuple): 
An ordered, immutable collection of items. Tuples are defined with parentheses, e.g., (1, 2, 3) or ('a', 'b', 'c').

🌀**_Example_**

```
# An example of a tuple
months_of_the_year = ("January", "February", "March", "April")
print("Months of the Year:", months_of_the_year)
```

### 6. Boolean (bool): 
Represents truth values. The two boolean values are True and False.


### 7. Set (set):
An unordered collection of unique items. Sets are defined with curly braces, e.g., {1, 2, 3} or {'apple', 'banana', 'cherry'}. Note that sets do not allow duplicate elements.

### 8. NoneType (None): 
A special type representing the absence of a value or a null value.

Each data type serves a specific purpose and can be used in different scenarios in Python programming. For instance, lists and tuples are great for storing ordered collections of items, dictionaries are ideal for storing related data as key-value pairs, and sets are useful for storing unique items and performing set operations.


[🔝](#Lesson-4-Data-types)
