---
title: Data Structures -  Lists, Tuples, Dictionaries, and Sets
date: 2023-05-06 12:00:00 -500
categories: [Python, Python Course]
tags: [python, datastructures, structures]     # TAG names should always be lowercase
---

In this blog post, we will dive into the world of Python data structures. We will explore lists, tuples, dictionaries, and sets, discussing their common operations and methods with illustrative code snippets.

## Table of Contents

1. Lists and Tuples

2. Dictionaries

3. Sets

4. Common Operations and Methods for Data Structures

## Lists and Tuples

Lists and tuples are both ordered collections of items that can store a variety of data types.

## Lists

A list is a mutable, ordered sequence of elements enclosed in square brackets [].
```python
#Creating a list
fruits = ['apple', 'banana', 'cherry']
print(fruits)

#You can perform several operations on lists, such as adding or removing elements.

#Adding an element to the list
fruits.append('orange')
print(fruits)

#Removing an element from the list
fruits.remove('banana')
print(fruits)
```
## Tuples

A tuple is an immutable, ordered sequence of elements enclosed in parentheses ().
```python
#Creating a tuple
coordinates = (12.5, 45.7)
print(coordinates)
```
As tuples are immutable, you cannot add or remove elements after they are created.
```python
#This will raise an error
coordinates[0] = 13.5
```
## Dictionaries

A dictionary is an unordered collection of key-value pairs enclosed in curly braces {}.
```python
#Creating a dictionary
student = {'name': 'John', 'age': 25, 'course': 'Computer Science'}
print(student)
```
You can `access`, `add`, or `modify` elements in a dictionary using their keys.
```python
#Accessing an element in the dictionary
print(student['name'])

#Adding a new key-value pair to the dictionary
student['grade'] = 'A'
print(student)

#Modifying the value of an existing key
student['age'] = 26
print(student)
```
## Sets

A set is an unordered collection of unique elements enclosed in curly braces {}.
```python
#Creating a set
prime_numbers = {2, 3, 5, 7, 11}
print(prime_numbers)
```
Sets do not support duplicate elements, so adding an existing element will not change the set.
```python
#Adding an element to the set
prime_numbers.add(13)
print(prime_numbers)

#Attempting to add a duplicate element
prime_numbers.add(5)
print(prime_numbers)  # No change
```
## Common Operations and Methods for Data Structures

***Here are some common operations and methods applicable to these data structures:***

`len()`: Returns the number of elements in a list, tuple, dictionary, or set.

`in`: Checks if an element exists in a list, tuple, dictionary (by key), or set.

`.update()`: Adds multiple elements to a set or updates a dictionary with new key-value pairs.

`.pop()`: Removes and returns the last element from a list or an arbitrary element from a set; removes and returns the value associated with a specified key in a dictionary.
```python
#Using len()
print(len(fruits))       # List
print(len(coordinates))  # Tuple
print(len(student))      # Dictionary
print(len(prime_numbers)) # Set

#Using 'in'
print('apple' in fruits)  # True

#Updating a set/dictionary
prime_numbers.update({17, 19})
print(prime_numbers)

student.update({'email': 'john@example.com'})
print(student)

#Using .pop()
last_fruit = fruits.pop()
print(last_fruit)
print(fruits)

random_prime = prime_numbers.pop()
print(random_prime)
print(prime_numbers)

age = student.pop('age')
print(age)
print(student)
```
In conclusion, Python offers a variety of data structures to efficiently store and manipulate data. Understanding lists, tuples, dictionaries, and sets, along with their common operations and methods, is essential for any Python developer.