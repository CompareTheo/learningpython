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
### More on Functions
- Using scripting langages to accomplish tasks in your work is akin to having LEGO bricks you can use to build the things you might need.
- However, you might not want to always rebult the same LEGO structures over and over again. Be that for use across a variety of projects, or because you might want to use the same functionality repeatedly witin the single project of your focus.
- To this point we have used several of the python built-in functions. However, it might be nice create our own functions!
- Creating your own functions are a great way to nicely package reusable blocks of code.
- A properly defined function consists of the following components.
  1. Keyword ```def``` that marks the start of the function header.
  2. A function name to uniquely identify the function. (Convention is all lowercase with an underscore to seperate words in the function name.)
  3. Parameters through which we pass values to a function. (These are optional.)
  4. A colon (:) to mark the end of the function header.
  5. One or more valid pythong statements that make up the function body. Statements must have the same indentation level (usually 4 spaces).

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
# Begin by defining our new function that will greet the user of our script. We are also including the name of the variable we will want to pass to the function for its use when the function is called.
def greet(name):
  # Use a formated string literal to easily format the string greeting we want to write to the screen.
    print(f"Hello, {name}. Good Morning!")
  # Use the same format as before, asking for, and assigning the user's input to a variable name.
name = input("What's your name? ")
# Call our function and pass it the variable name.
greet(name)
```
- Notice again that everything under ```def greet``` is indented.
- Python is an indented langage. It uses indentation to understanding what is part of the above fuction. Therefore, everything in the ```hello``` function must be indented.