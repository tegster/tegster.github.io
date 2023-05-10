---
title: Web Scraping
date: 2023-05-09 12:00:00 -500
categories: [Python, Python Course]
tags: [python, oop, objectoriented]     # TAG names should always be lowercase
---

## Table of Contents:

1. Introduction to Web Scraping
2. Using BeautifulSoup and Requests Libraries
3. Scraping Data from Websites
4. Storing and Processing Scraped Data

## Introduction to Web Scraping

Web scraping is the process of extracting data from websites for various purposes such as data analysis, content aggregation, or information retrieval. In this blog post, we will explore web scraping in Python using the BeautifulSoup and requests libraries. 

## Using BeautifulSoup and Requests Libraries

To start web scraping in Python, you need to install the BeautifulSoup and requests libraries. You can do this using `pip:`
```console
pip install beautifulsoup4 requests
```
## Requests

The requests library allows you to make HTTP requests in Python. You can use it to fetch the HTML content of a webpage.
```python
import requests

url = "https://example.com"
response = requests.get(url)

print(response.status_code)  # Output: 200
print(response.text)
```
In this code snippet, we import the requests library and use the `get()` function to fetch the HTML content of a webpage. The `status_code` attribute indicates the HTTP status of the request (200 means success), and the text attribute contains the HTML content.

## BeautifulSoup

BeautifulSoup is a library that helps you parse and navigate HTML and XML documents.
```python
from bs4 import BeautifulSoup

html_doc = """

        Example Page

        Welcome to the Example Page
        This is an example paragraph.


"""

soup = BeautifulSoup(html_doc, "html.parser")

print(soup.title)  # Output: Example Page
print(soup.h1)     # Output: Welcome to the Example Page
```
In this code snippet, we import the BeautifulSoup class from the bs4 library and create a BeautifulSoup object using the html_doc string. We then access the title and h1 elements of the HTML document.

## Scraping Data from Websites

Now let's fetch the HTML content of a webpage using requests and parse it using BeautifulSoup.
```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"
response = requests.get(url)

soup = BeautifulSoup(response.text, "html.parser")
```
In this code snippet, we fetch the HTML content of the example.com webpage and create a BeautifulSoup object to parse the content.

Next, let's extract some data from the parsed HTML. For example, let's find all the paragraph elements (``).
```python
paragraphs = soup.find_all("p")

for p in paragraphs:
    print(p.text)
```
Here, we use the `find_all()` method to find all the paragraph elements in the HTML document and print their text content.

## Storing and Processing Scraped Data

Once you have scraped the data from a webpage, you can store it in various formats such as JSON, CSV, or a database for further processing and analysis.

In this example, let's store the extracted paragraph texts in a JSON file using the json module.
```python
import json

data = [p.text for p in paragraphs]

with open("paragraphs.json", "w") as file:
    json.dump(data, file)
```
In this code snippet, we created a list of paragraph texts using a list comprehension and write it to a JSON file named paragraphs.json using the json.dump() function.

To read the stored data back into your Python script, you can use the `json.load()` function.
```python
with open("paragraphs.json", "r") as file:
    data = json.load(file)

print(data)
```
Here, we read the JSON data from the `paragraphs.json` file and store it in a list named `data`.

In conclusion, web scraping in Python using the BeautifulSoup and requests libraries allows you to extract information from websites and store it for further processing and analysis. Happy Coding!