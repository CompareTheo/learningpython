---
layout: default
title: 01 - Functions and Variables
nav_order: 2
---
### Agenda:
- 00-Getting Started Recap
- Parameters & Arguments
- Formatting Strings or str
- Commenting Code
- Integers or int
- Floating Point Numbers
- Homework
---
### Key Terms:
- **Function** - The LEGO blocks of code that execute as a part of your program are called functions.
- **Variable** - A parameter that is mutable. Meaning its value can be reassigned.
- **Parameter** - Arguments taken by a function.
---
### 00-Getting Started Recap
- We installed python and began to get comfortable with some basic Windows Shell commands. [Commands Cheat Sheet](https://lmu.box.com/s/tzbhj6y6366jyob1an4chafwzlj8katl)
- Using these commands, we created a directory from which we will store and run all the code we write during these tutorials.
- Our first coding project used the built-in print function *print()* to print "Hello, World!" to the screen.
- This lead to an exploration of other built-in functions including *input()* which will allow the user to provide an input to the program.
- We assigned that input to a variable called "name" and then talked about how to print that name back to the screen.
```python
name = input("What's your name? ")
print("Hello, ")
print(name)
```
- Ultimately, we ended up with a script that would (rather crudely) say "Hello, Jason", substituting the user's input as the sentience's subject.
- We concluded our discussion with a tease of the default arguments assigned in the *print()* function and hinted at various ways to structure our returned string.
---
### Parameters & Arguments
- Let's open hello.py and rewind a bit and examine the visual side effect of having the results of our Hello World program appear on separate lines. We discussed this side effect in brief last week, but I want to re-examine it today for discussion in greater detail. 
```python
name = input("What's your name? ")
print("Hello, ")
print(name)
```
- Last week, we were bothered by the fact that our assigned variable *name* was printed to the screen on a separate line.
- One of the ways to influence this behavior, is to include an argument to modify the functions behavior.
- Looking at the [python documentation for the print function](https://docs.python.org/3/library/functions.html#print) we see that the print function takes an argument called *end* which, in its default state, will insert a new line (/n) after the function has returned its value.
- By modifying the parameter of this argument in our function's first call, we can change the behavior of our program.
```python
name = input("What's your name? ")
print("Hello, " end="")
print(name)
```
- By providing *end=""* we are over-writing the default value of *end* such that it never creates a new line after this first print statement.
- Parameters, therefore, are arguments that can be take by a function.
---
### Formatting Strings or str
- I will briefly mention that you should be very careful about the use of quotation marks when formatting strings. Let's take a look at an errant example. 
```python
print("hello,"friend"")
```
- Notice how adding quotation marks as part of you strings can be challenging. This is a common challenge for many programmers and general convention would have you avoid it where possible.
- Instead, general convention in the post python 3.6 era would have you use "formatted string literals" or "f-strings" when attempting to print formatted text to the screen.
```python
name = input("What's your name? ")
print(f"hello, {name}")
```
- Notice the f in ```Print(f"hello, {name}")```. This f is a special indicator to Python to treat this string in a special way. Going forward, this is going to be our preferred method for printing formatted strings to the screen.
- In all of our collective experience working with computers, forms, other people and their use of our forms... we all know that... you should never expect that your user will cooperate with your inputs as you intended when writing the code.
- Therefore, you will need to ensure that the input of your user is corrected or checked. It turns out that built into the string type is the ability to do several of these things. Let's explore some of the more common methods for cleaning up or pre-formatting user provided data. 
- One of the most common errors to correct for when accepting strings is to remove whitespace.
- By utilizing the method *strip* on *name*, it will strip all the whitespaces on the left and right of the users input. 
```python
name = input("What's your name? ")
name = name.strip()
print(f"hello, {name}")
```
- Rerunning this program, regardless of how many spaces you type before or after the name, it will strip off all the whitespace. 
- Because we are collecting names, it might be beneficial to ensure that the name is capitalized so that the greeting reads correctly. 
- Using the *title* method, it would title case the user's name.
```python
name = input ("What's your name? ")
name = name.strip()
name = name.title()
print(f"hello, {name}")
```
- Yes, it is possible to stack methods in your code. Having different methods act on the same variable is not uncommon, however, caution should be taken when stacking them. Python executes code from top to bottom, left to right, the same way we read in American English. 
- Yet, there is still a more efficient way to format this code. To make it more pythonic.
```python
name = input ("What's your name? ")
name = name.strip().title()
print(f"hello, {name}")
```
- This creates the same results as your previous code... but we can go even one step further.
```python
name = input("What's your name? ").strip().title()
print(f"hello, {name}")
```
- This works because of the way methods interact with functions.
- Ok... enough about strings.
---
### Commenting Code
- Comments are in integral part of any program. They can come in the form of module-level docstrings, or even inline explanations that help shed light on a complex function.
- Comments serve two important functions: they help you remember what the code does, and they create a corpus of knowledge that other developers can skim to gain an understanding of how it all works very quickly. 
- My big advice is EXCESSIVELY COMMENT YOUR CODE. You will forget what things do in your code or why you make the decision that you made... it is important to have those decisions canonized for your future self.
- To write a comment in Python, simply put the hash mark *#* before your desired comment. Python ignores everything after the hash mark and up to the end of the line.
- You can insert them anywhere in your code, even in line with other code. Them location of your comment tags will be a personal stylistic choice that you will make as a coder.
- Comments should be short, sweet, and to the point. A max of 72 characters per comment line is the standard.
- You will be expected to comment ALL code going forward.
---
### Integers or int
- In Python, an integer is referred to as an int.
- In the world of mathematics, we are familiar with +,-,*,/, and % operators. That last operator % or modulo operator may not be very familiar to you... but we will cover it in time. 
- Python understands numbers or integers almost in the same ways that we as humans do. Meaning, it sees a number and recognizes that it can perform those same arithmetic operators on those numbers, just like humans.
- Let's start a new python file called *calculator.py*. This will be our new file where we explore using python to complete some calculations and learn about integers.
- Let's start by defining a few variables and doing some simple addition.
```python
x = 1
y = 2
z = x + y
print(z)
```
- Naturally, when we run *python calculator.py* we get the result in the terminal window of 3. However, We can make this more interactive using the input function.
```python
x = input("What's x? ")
y = input("What's y? ")
z = x + y
print(z)
```
- oops... running this program, we discover that the output is incorrect as 12. We discussed this in brief last week... do you know why?
- Last week, we saw how the + sign concatenates two strings. Because your input from your keyboard comes into the computer as text, it is treaded as a string. We, therefore, need to convert this input to that of another type. From string to integer. 
```python
x = input("What's x? ")
y = input("What's y? ")
z = int(x) + int(y)
print(z)
```
- The result shown is now correct. The use of int(x), is called "casting" where a value is temporarily changed from one type of variable (in this case, string) to another (here, an integer).
- And to further clean this up, much like you can run multiple methods on a function, you can also call multiple functions on a function.
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
print(x + y)
```
- The most inner function is run first, then the outer one is run. First, the input function is run. Then, the int function.
- I think it is becoming most obvious from our many examples that there are many ways to solve a coding task. Which approach you take to programming is less important then that you make your code readable. You should use comments to give yourself and others clues about what you code is doing. Further, you should create code in a way that is readable.
---
### Floating Point Numbers
- So we have discussed integers. But integers are whole real numbers and that type will not resolve numbers to their nearest decimal place; instead choosing to round to the nearest whole.
- A floating point value is a real number that has a decimal point in it, such as 0.52
- You can change your code to support floating point numbers by changing your input type to float.
```python
x = float(input("What's x? "))
y = float(input("What's y? "))
print(x + y)
```
- This change allows your user to enter 1.2 and 3.4 to present a total of 4.6
- Let’s imagine, however, that you want to round the total to the nearest integer. Looking at the Python documentation for round you’ll see that the available arguments are ```round(number[n, ndigits])```. Those square brackets indicate that something optional can be specified by the programmer. Therefore, you could do ```round(n)``` to round a digit to its nearest integer. Alternatively, you could code as follows:
```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Create a rounded result
z = round(x + y)

# Print the result
print(z)
```
- The output will be rounded to the nearest integer.
- What if we wanted to format the output of long numbers? For example, rather than seeing 1000, you may wish to see 1,000. You could modify your code as follows:
```python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Create a rounded result
z = round(x + y)

# Print the formatted result
print(f"{z:,}")
```
- Though quite cryptic, that ```print(f"{z:,}")``` creates a scenario where the outputted z will include commas where the result could look like 1,000 or 2,500. 
---
### **Homework**
---
#### The "Weight" of Mr. Einstein
You might have heard that E = mc^2, wherein E represents energy (measured in Joules), m represents mass (measured in kilograms), and c represents the speed of light (measured approximately as 300000000 meters per second), per Albert Einstein et al. 

In a file called einstein.py, implement a program in Python that prompts the user for mass as an integer (in kilograms) and then outputs the equivalent number of Joules as an integer. Assume that the user will input an integer.

##### Homework Hints
- Recall that input returns a str.
- Recall that int can convert a str to an int.
- Recall that Python comes with several built-in functions.
