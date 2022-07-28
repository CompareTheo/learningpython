---
layout: default
title: 03 - Conditions and Control Flow
nav_order: 4
---
# [](#01-Functions)03 - Conditionals and Control Flow
### [](#Agenda)Lesson Outline:
- 01 - Recap
- Homework Review
- Defining Functions
- Conditionals
- Homework

---
### 02- Recap
- Last week we discussed ways to influence the behavior of our functions by modifying the arguments that the function takes.
```python
name = input("What's your name? ")
print("Hello, " end="")
print(name)
```
- By providing ```end=""``` we are over-writing the default value of ```end``` such that it never creates a new line after this first print statement.
- We also learned about the joys of "formatted sting literals" or "f-strings" to assist with formatting strings printed to the screen.
```python
name = input("What's your name? ")
print(f"hello, {name}")
```
- Further, we explored two numeric data types in python, integers (int) and floats (float). 
- Remember that python understands both integers and floats in the same way that humans do and is capable of seeing these characters as strings, integers, or floats. Thus, performing the required fuctions available to each type, including arithmetic fuctions.

---
### Homework Review
#### The "Weight" of Mr. Einstein

You might have heard that E = mc^2, wherein E represents energy (measured in Joules), m represents mass (measured in kilograms), and c represents the speed of light (measured approximately as 300000000 meters per second), per Albert Einstein et al. 

In a file called einstein.py, implement a program in Python that prompts the user for mass as an integer (in kilograms) and then outputs the equivalent number of Joules as an integer. Assume that the user will input an integer.


#### Homework Check
<script id="asciicast-vRmCPKq2FVw0LqrT6hc3QU4q7" src="https://asciinema.org/a/vRmCPKq2FVw0LqrT6hc3QU4q7.js" async data-autoplay="1" data-loop="1" data-speed="2" data-rows="4" data-cols="80"></script>

---
### Defining Functions
- To this point we have used several of the python built-in functions. However, it might be nice create our own functions!
- Creating your own functions are a great way to nicely package reusable blocks of code. 
- Let's begin by looking at the last version of hello.py we discussed in the last session.
```python
# Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
name = input("What's your name? ").strip().title()
# Print the output
print(f"hello, {name}")
```
- It might be possible to better our code by creating our own special function that says "hello" for us.
- Let's start from scratch:
```python
def hello()
  print("hello")
  
name = input("What's your name? ")
hello()
print(name)
```
