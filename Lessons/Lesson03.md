# Lesson 3 Coding Basics

### Key concepts

* [Comments vs. codes, Run code cell](#Comments-vs-codes)
* [Input vs. output](#Input-vs-output)
* [Variables](#Variables)
* [Operators](#Operators)
* [Functions](#Functions)
* [Modules, libraries & packages](#module-library-package)

[🔝](#Lesson-3-Coding-Basics)
### Sample

![](https://github.com/MK316/Coding4ET/raw/main/images/image07.png)


[🔝](#Lesson-3-Coding-Basics)

## Comments vs codes

```
# This is a comment line

print("Hello, Python!") # this is a code line
```


[🔝](#Lesson-3-Coding-Basics)


## Input vs Output



[🔝](#Lesson-3-Coding-Basics)

## Operators



[🔝](#Lesson-3-Coding-Basics)

## Variables


[🔝](#Lesson-3-Coding-Basics)

## Functions


[🔝](#Lesson-3-Coding-Basics)

## Module-library-package

**Modules:** Think of a module as a single file containing Python code. It might contain functions, variables, and classes which you can use once you import this module into your own code. It's like a toolbox that has a specific set of tools you can use.

**Packages:** A package is a collection of Python modules under a common namespace. This usually means they are in the same folder and are related to each other in some way. You can think of a package as a bigger toolbox that holds several smaller toolboxes (modules). 

**Libraries:** A library is a more general term that refers to a collection of packages and modules. It's like a big bookshelf where you store all kinds of toolboxes and individual tools. You can import these libraries into your programs and use the functions and classes that they offer. Sometimes people use 'library' and 'package' interchangeably.

In summary, a module is a single file, a package is a collection of these files, and a library is a collection of packages and modules. They all help you to leverage existing code for your own projects, making programming in Python much more efficient and powerful.

## 🐥 Import or install packages
To demonstrate how to import a package and pick a random number from 1 to 10 in Python, you can use the random module. This module is a part of the standard Python library, so you don't need to install anything extra. Here's a simple example:

```
# Generate a random number between 1 and 10

random_number = random.randint(1, 10)

print("The random number is:", random_number)
```

## Examine the differences

Variable at the end vs. print(variable)

```
# Code 1

random_number = random.randint(1, 10)

random_number
```

```
# Code 2

random_number = random.randint(1, 10)

random_number
print(random_number)
```

```
# Code 3

random_number = random.randint(1, 10)

print(random_number)
random_number
```

```
# Code 4

random_number = random.randint(1, 10)

print("random_number:", random_number)
```

```
# Code 5

random_number = random.randint(1, 10)

print("The random number is: ", random_number)
```


[🔝](#Lesson-3-Coding-Basics)
