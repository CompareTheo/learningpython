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
- With Keyword

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

---
### File I/O Overview
- Up until now, everything we've programmed has stored information in memory. That is, once the program is ended, all information gathered from the user or generaged by the program is lost.
- File I/O is the ability of a program to take a file as input or create a file as output.

---
### Open Function
- ```open``` is a function that is built into Python that allows you to open a file and utilize it in your program.
- The ```open``` function allows you to open a file such that you can read from it or write to it.
- Let us look at a simple example to show how to enable file I/O in your program. 
```python
name = input("What is your name? ")
file = open("names.txt", "w")
file.write(name)
file.close()
```
- Notice that the ```open``` function optens a file called ```names.txt``` with writing enabled, as signified by the ```w```. The code above assigns that opened file to a variable called ```file```.
- The line ```file.write(name)``` writes the name to the text file. The line after closes that file.
- Testing out your code, you will notice that, as written, your program will entirely rewrite the ```names.txt``` file each time.
- Ideally, we want to be able to append each of our names to the file. In order to do that, we must modify our code as follows:
```python
name = input("What is your name? ")
file = open("names.txt", "a")
file.write(name)
file.close()
```
- Note that the only change to our code is that the ```w``` "write" has been changed to an ```a``` for "append".
- After running this program with multiple names, you might notice that all of the names are running together. The names are being appended without any gaps between each of the names. Here's how we fix that issue.
```python
name = input("What is your name? ")
file = open("names.txt", "a")
file.write(f"{name}\n")
file.close()
```
- Notice that the line with ```file.write``` has been motified to use an ```f-string``` and to include a line break at the end of each name. 

---
### With Keyword
- The keyword ```with``` allows you to automate the closing of a file.
```python
name = input("What is your name? ")
with open("names.txt", "a") as file:
    file.write(f"{name}\n")
```
- Take note that the line below ```with``` is indented.
- To this point, we have been exclusivly writing to a file. What if we wanted to read from a file. 
```python
with open("names.txt", "r") as file:
    lines = file.readlines()
for line in lines:
    print("hello ", line)
```
- Notice that ```readlines``` has a special ability to read all the lines of a file and store them in a file called lines.
- Running your program, you will notice that the output is quite ugly. There seem to be multiple line breaks where there should be only one.
- There are many approaches to fix this issue. However, here is one simple way:
```python
with open("names.txt", "r") as file:
    lines = file.readlines()
for line in lines:
    print("hello ", line.rstrip())
```
