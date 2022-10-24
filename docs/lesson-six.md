---
layout: default
title: 06 - Libraries and File I/O
nav_order: 7
nav_exclude: false
---
# 06 - Libraries and File I/O
### Lesson Outline:
- Libraries
- Command-Line Arguments
- Open Function
- With Function
- CSVs

---
### Libraries
- In general, libaries are bits of code that are written by you or others that you can reuse in our program.
- Python allows you to share functions or features with others as "modules."
- If you find yourself copy and pasting code from an old project, you should consider creating a module or library that you could bring into your new project.
- The standard python installer comes with some libraries that you can import into your own project. 
- As a coder you should feel no shame in standing on the sholders of other coders.
- Let's play with a library that comes with Python called ```random```. 
- So, how do you load a module into your own program? You can use the word ```import``` in your program.
- Inside the ```random``` module, there is a built-in function called ```random.choice(seq)```. 
- ```random``` is the module you are importing. 
- Inside that moddule, there is a ```choice``` function. That function takes into it a sequence that is a list.
```python
import random
coin = random.choice(["heads", "tails"])
print(coin)
```
- Notice that the list within ```choice``` has square braces, quotes, and a comma.
- Moving on, consider the function ```random.randint(a, b)```. This function will generate a random number between ```a``` and ```b```.
```python
import random
number = random.randint(1, 10)
print(number)
```
- So far, we have been prividing all values within the program that we have created.
- What if we wanted to be able to take the input from the command-line?

---
### Command-Line Arguments
- For example, rather than typing ```python average.py``` in the terminal, what if we wanted to be able to type ```python average.py 100 90``` and be able to get the average between 100 and 90?
- ```sys``` is a module that allows us to take arguments at the command line.
- ```argv``` is a function within the ```sys``` module that allows us to learn about what the user typed in at the command line. Notice how you will see ```sys.argv``` utilized in the code below.
```python
import sys
print("Hello, my name is ", sys.argv[1])
```
- Notice that the program is going to look at what the user typed in the command line.
- Currently, if you run the program by typing ```python name.py Jason``` into the terminal window, you will see ```Hello, my name is Jason```. 
- You can learn more in Python's documentation of [```sys```](https://docs.python.org/3/library/sys.html)