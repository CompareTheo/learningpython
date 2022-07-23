---
layout: default
title: 01 - "Hello, World!"
nav_order: 2
---
# [](#01-Functions)01 - "Hello, World!"
### [](#Agenda)Lesson Outline:
- Installing Notepad ++ for Windows.
- Introduction to the Windows Shell
- Setting Up the Tutorial Environment
- Functions & Hello, World!
- Introducing Variables

---
### Installing Notepad++  for Windows
- Download [Notepad++](https://notepad-plus-plus.org/downloads/)
- You will want to download the 64-bit installer link to use the graphical installer with prompts.
- Choose Installer language "English"
- Follow the on-screen prompts; accepting all of the default settings to install Notepad++. 
- You do not need to open Notepad++ once the installer has completed. We will open it later as a part of the tutorial.

---
### Introduction to the Windows Shell
- Windows PowerShell is a configuration management tool that brings some of the capabilities of the Linux command-line interface (CLI) control into the historically point-and-click Windows environment to manage Windows servers. 
- Bash is the shell most common to other computer operating systems like Mac and Linux. Bash is more traditionally suited for development environments. However, because setting up true development environments are outside the scope of this tutorial, we are going to forgo installing a bash shell in our local Windows environments. 
- Instead, we will take advantage of the Bash commands that are built into Windows PowerShell as a part of its capabilities as a Linux CLI. While these commands may not seem immediately useful, in my experience, it is helpful to have some basic comfort with the command line interface as it is the environment in which your scripts will run, as for input, and present errors. 
- In an effort to become comfortable with the Windows Shell environment, we are going to setup our tutorial folder structure using only Windows PowerShell.
- Changing directories = cd
- Creating "directories" or "folders" = mkdir nameofdirectory
- Making a file = New-Item nameofitem.extention
- Make a folder for the tutorials in the directory of your choice. 
- Create a hello.py file to complete today's tutorial.

---
### Functions & "Hello, World!"
- A function is a block of code which only runs when it is called. You can pass data, known as parameters into a function. A function can return data as a result.
- Python has catalog of build in functions, some of which we will explore today in our foray into the pythonic typed structure.
![](../../assets/images/small-image.png)
- In this tutorial, we are going to begin by using the ```print()``` function and walk through the most common beginner program in all of computer programming. 
- Open hello.py (created before) in Notepad++
```python
print("Hello, world!")
```
- ```print()``` [documentation](https://docs.python.org/3/library/functions.html#print)
- ```input()``` [documentation](https://docs.python.org/3/library/functions.html#input)
```python
input("What's your name? ")
print("Hello, world!")
```
- This edit alone, however, will not allow your program to output what your user inputs. For that, we will need to introduce variables.

---
### Introducing Variables
- A variable is just a container for a value within your own program.
- In your program, you can introduce your own variable in your program by editing it to read:]
```python
name = input("What's your name? ")
print("hello, world")
```
- Notice that this equal sign in the middle of ```name = input("What's your name? ")``` has a special role in programming. This equal sign literally assigns what is on the right to what is on the left. Therefore, the value returned by ```input("What's your name? ")``` is assigned to name.
- However, we are still not using the "name" variable in our code. The variable is being assigned but not used.
- It would seem logical to try:
```python
name = input("What's your name? ")
print("hello, name")
```
- But this only returns the string "name," we are still not using the variable itself. 
- There are two ways to use the variable in this case:
```python
print("hello, " + name)
print("hello, ", name) #print is a function that takes multiple arguments, so you can simply use a comma. 
```
