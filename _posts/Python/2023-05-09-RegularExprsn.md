---
title: Regular Expressions in Python
date: 2023-05-09 12:00:00 -500
categories: [Python, Python Course]
tags: [python, oop, objectoriented]     # TAG names should always be lowercase
---

# Mastering Regular Expressions in Python

Table of Contents:

1. Introduction to Regular Expressions
2. The re Module in Python
3. Pattern Matching and Substitution

## Introduction to Regular Expressions

Regular expressions (regex) are a powerful tool for working with text data. They allow you to search, match, and manipulate strings based on patterns. In this blog post, we will explore regular expressions in Python using the re module. We will cover pattern matching and substitution with code snippets and explanations.

## The re Module in Python

Python provides the built-in re module for working with regular expressions. To use it, you need to import the module first.

```python
import re
```
## Pattern Matching and Substitution

Pattern Matching

The re module provides several functions for pattern matching, such as `search()`, `match()`, and `findall()`.
```python
import re

text = "Python is an amazing programming language."

#Search for the pattern 'Python' in the text
result = re.search("Python", text)

if result:
    print("Pattern found!")
else:
    print("Pattern not found")
```
In this code snippet, we use the `re.search()` function to search for the pattern "Python" in the given text. If the pattern is found, the function returns a match object; otherwise, it returns None.

Using `re.match()` to find a pattern at the beginning of the string
```python
result = re.match("Python", text)

if result:
    print("Pattern found!")
else:
    print("Pattern not found")
```
Here, we use the `re.match()` function to check if the pattern "Python" is present at the beginning of the given text.

Using `re.findall()` to find all occurrences of a pattern
`pattern = r"\b\w{5}\b"`  # Matches any 5-letter word
`words = re.findall(pattern, text)`

print(words)  # Output: ['Python']

In this example, we use the `re.findall()` function to find all occurrences of 5-letter words in the given text. The pattern `\b\w{5}\b` matches any word with exactly 5 characters.

## Substitution

The `re.sub()` function allows you to replace occurrences of a pattern with a specified string.

```python
import re

text = "Python is an amazing programming language."

Replace 'Python' with 'Java'
new_text = re.sub("Python", "Java", text)

print(new_text)  # Output: Java is an amazing programming language.
```
In this code snippet, we use the `re.sub()` function to replace the pattern "Python" with "Java" in the given text.

You can also use capturing groups and backreferences to perform more advanced substitutions.

```python
text = "12-34-56"

#Rearrange the numbers using capturing groups and backreferences
pattern = r"(\d{2})-(\d{2})-(\d{2})"
replacement = r"\3-\1-\2"
new_text = re.sub(pattern, replacement, text)

print(new_text)  # Output: 56-12-34
```
In this example, we use capturing groups (denoted by parentheses) to match each pair of digits in the text. We then use backreferences (such as \1, \2, and \3) in the replacement string to rearrange the matched digits.

In conclusion, regular expressions are a powerful tool for working with text data in Python. By mastering the re module's pattern matching and substitution functions, you can efficiently search, match, and manipulate strings based on patterns.