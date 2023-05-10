---
title: Functions and Modules
date: 2023-05-05 12:00:00 -500
categories: [Python, Python Course]
tags: [python, functions, modules]     # TAG names should always be lowercase
---

# Functions and Modules

Introduction
In this blog post, we'll explore the role of functions and modules in Python, how to define and call functions, work with function arguments, and import modules. Let's get started!


## Table of Contents

1. Defining and Calling Functions

2. Function Arguments and Return Values

3. Variable Scope

4. Importing Modules and Using Built-in Functions

5. Conclusion


## Defining and Calling Functions

Functions are reusable blocks of code that perform a specific task. They help make your code more modular and easier to maintain. To define a function in Python, use the def keyword followed by the function name and a pair of parentheses:
```python
# Defining a simple function
def greet():
    print("Hello, World!")

# Calling the function
greet()
```
In this example, we've created a simple function called greet() that prints "Hello, World!" when called.

## Function Arguments and Return Values
Functions can accept input values, known as arguments, and return output values. You can specify the arguments inside the parentheses during the function definition and use the return keyword to return a value.
```python
#Defining a function with arguments and a return value
def add(a, b):
    return a + b

#Calling the function with arguments
result = add(3, 5)
print(result)  # Output: 8
```
In this example, we've defined an `add()` function that accepts two arguments `(a and b)` and returns their sum.

## Variable Scope
Variables in Python have either local or global scope, depending on where they are defined. Variables defined inside a function have a local scope and can only be accessed within that function. Variables defined outside a function have a global scope and can be accessed throughout the entire program.

```python
#Global variable
global_var = "I'm a global variable."

def my_function():
    #Local variable
    local_var = "I'm a local variable."
    print(global_var)
    print(local_var)

my_function()

Output:
I'm a global variable.
I'm a local variable.

```
This will raise an error, as local_var is not accessible outside the function
print(local_var)

## Importing Modules and Using Built-in Functions
Python has a vast library of built-in functions and modules that you can use to enhance your code. To use a module, you need to import it using the import keyword.
```python
#Importing the math module
import math

#Using a function from the math module
result = math.sqrt(16)
print(result)  # Output: 4.0

#Importing a specific function from a module
from math import sqrt

result = sqrt(25)
print(result)  # Output: 5.0
```
In this example, we've imported the math module and used its `sqrt()` function to calculate the square root of a number.

## Conclusion
In this blog post, we've covered the fundamentals of functions and modules in Python, including defining and calling functions, working with function arguments, understanding variable scope, and importing modules. Happy coding!