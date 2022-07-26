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

---
### Homework Review
#### The "Weight" of Mr. Einstein

You might have heard that E = mc^2, wherein E represents energy (measured in Joules), m represents mass (measured in kilograms), and c represents the speed of light (measured approximately as 300000000 meters per second), per Albert Einstein et al. 

In a file called einstein.py, implement a program in Python that prompts the user for mass as an integer (in kilograms) and then outputs the equivalent number of Joules as an integer. Assume that the user will input an integer.

##### Homework Hints
- Recall that input returns a str.
- Recall that int can convert a str to an int.
- Recall that Python comes with several built-in functions.

#### Homework Check
<script id="asciicast-vRmCPKq2FVw0LqrT6hc3QU4q7" src="https://asciinema.org/a/vRmCPKq2FVw0LqrT6hc3QU4q7.js" async></script>
