---
title: Python - Variables and Data Types
date: 2023-05-02 12:00:00 -500
categories: [Python, Python Course]
tags: [python, variables, python variable, datatype]     # TAG names should always be lowercase
---

# Topics to Teach for Variables in Python

## What are variables
A variable is a named location in memory that stores a value.

## Why variables are important

Variables allow us to store and manipulate data in our programs.

**Example of a variable in Python**
```python
x = 5
```
## Variable declaration:

Declare a variable called my_variable with a value of 10
    
```python
my_variable = 10
```

## Variable naming conventions:

**Example of following variable naming conventions**

```python
first_name = "John"

last_name = "Doe"

full_name = f"{first_name} {last_name}"
```

## Variable assignment and reassignment:

**Example of assigning a new value to a variable**

```python
x = 5

x = 10

print(x) # Output: 10
```


# Data types in Python
 
 Data type are a pre-defined type of variable that specifies the kind of data that can be stored in it. By using different data types in your program, you can manipulate and process different kinds of data, such as numbers, text, and logical values.

 Again, a data type is a just way to classify different types of data in a program, while a variable is a container that holds a value and is assigned a specific data type.

 Lets take a look at different types of Data Types that exist. 

## Integers
Integers are considered as Whole numbers, such as 3, -5, and 0.

```python
x = 3
y = -5
```
## Floats
Floats are considered numbers with decimal points, such as 3.14, -2.5, and 0.0.

```python
pi = 3.14
temperature = -2.5
```
## Strings
Description: Text data, such as "hello world", "42", and "Python is fun".

```python
greeting = "Hello, world!"
message = 'Python is fun'
```

## Booleans
Booleans are Logical values that can be either True or False and that's it. Just true and false, that's it.

```python
is_raining = True
is_sunny = False
```
## Advanced Data Types
## Lists
Lists can be any ordered collections of data, such as [1, 2, 3], ["apple", "banana", "orange"], and [1, "hello", True]. Think of your grocery List, instead of just visiting the grocery store, maybe you write 'I need to say Hello to one person', now that's an item in your list.

```python
numbers = [1, 2, 3, 4, 5]
fruits = ["apple", "banana", "orange"]
```

## Tuples
Immutable ordered collections of data, similar to lists but cannot be changed once created, such as (1, 2, 3), ("apple", "banana", "orange"), and (1, "hello", True). Imagine lists but tuples cannot be changed.

```python
person = ("John", 30, "male")
point = (1, 2)
```

## Dictionaries
Dictionaries are Unordered collections of key-value pairs, such as {"name": "John", "age": 30}, {"fruit": "apple", "color": "red"}, and {"is_raining": True, "temperature": 20}.

Imagine, a whole variable and its value, stored in a list. variable is the key and Value is the value of the variable

```python
person = {"name": "John", "age": 30, "gender": "male"}
fruit_colors = {"apple": "red", "banana": "yellow", "orange": "orange"}
```


## Variable scope:

**Example of variable scope in Python**

```python
x = 5 # This variable has global scope

def my_function():

    x = 10 # This variable has local scope within the function
    print(x)

my_function() # Output: 10

print(x) # Output: 5

```

## String formatting with variables

**Example of string formatting with variables**

```python
name = "John"

age = 25

print(f"My name is {name} and I am {age} years old.")
```
## Constants:

**Example of declaring a constant in Python**

```python
MY_CONSTANT = 3.14
```
## Best practices:

**Example of using descriptive variable names and initializing variables**

```python
person_name = "John Doe"

num_of_items = 10

is_active = True
```
