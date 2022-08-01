---
layout: default
title: 03 - Conditions and Control Flow
nav_order: 4
---
# [](#01-Functions)03 - Conditionals and Control Flow
### [](#Agenda)Lesson Outline:
- 02 - Recap
- Homework Review
- Defining Functions
- Returning Values
- Libraries
- Conditionals
- if Statements
- Control Flow, elif, and else
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
name = input("What's your name? ").strip().title()
# Call our function and pass it the variable name.
greet(name)
```
- Notice again that everything under ```def greet``` is indented.
- Python is an indented langage. It uses indentation to understanding what is part of the above fuction. Therefore, everything in the ```greet``` function must be indented.

---
### Returning Values
- You can imagine many scenarios where you don't just want a function to perform an action, but also to return a value back to the main function.
- That is to say, we might want a function to perform an action using the returned value of a seperate function in our code. In the example below, a more "reusable" seperate function.
- Let's build a calculator to compute the square of a user provided number. 
- We start by defining the main function of our code. The major actions that our code should take on execution.
```python
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))
```
- This code should be fairly clear to this point. However, you might be asking youself, "Can python just square something? Is square a function I can use?" 
- In fact, you might have been asking that during the pervious homework assignment too and googling found that there is no such function in Python.
- The way mathematically that numbers are squared is to multiply the number by itself.
- So because, as a part of our main function, we have called a function ```square``` we need to define that function for our code to complete. 
```python
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))
def square(n):
    return n * n
main()
```
- Rather than simply printing the calculation of ```n * n```, you may want a function to retun the value of this caluclation back to another part of your program. This "passing back" of a value we call a ```return``` value.
- Effectively, ```x``` is passed to ```square```. Then, the calculation of ```x * x``` is retuned back to the main function.
- This will allow us to wholesale reuse this square function over and over again, but in our current script and in any future scripts we might write.

---
### Libraries
- A (software) library is a collection of modules that contain fuctions for use by other programs. 
- The [Python standard library](https://docs.python.org/3/library/) is a suite of modules that come with Python itself.
- Many additional libraries are available from [PyPI](https://pypi.org/) the Python Package Index.
- Two major take aways from this discussion are:
  1. Python libraries allow you to extend the functionality of your scripts beyond that which is "standard" within the context of installed Python. You can use other people's code in your own scripts.
  2. By writing our own functions, we can create custom libraries of our own to complete repetative (often challenging) tasks across many different coding projects we might be working on.

- We are not going to spend a ton of time on Python libraries yet, but I wanted to make you aware that they exists. 
- I do not encourage the use of libraries yet, and will not provide an example of their use until we are sufficiently ready for their use. 

---
### Conditionals
- Conditionals allow you, the programmer, to allow your program to make decisions.
- Built within Python are a set of "operators" that are used to ask mathematical questions. (Different from mathamatical operators which perform an arethmetic function, these operators allow you to ask math based questions.)
- Most of these will be very familure to you from other parts of your life. 
- ```> and <``` symbols are already quite familure to you.
- ```>=``` denotes "greater than or equal to."
- ```<=``` denotes "less than or equal to."
- ```==``` denotes "equals" although, special attention to be paid to the fact that this is a double equal sign as a single equal sign would assign a value.
- ```!=``` denotes "not equal to". 
- Conditional statements compare a left-hand term to a right-hand turm.

---
### if Statements
- The most common way to use conditionals is through activation in an if statement to query the results of a comparison.
- Opening ```compare.py``` let's create the following example.
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x < y:
    print("x is less than y")
```
- Notice how your code takes the input of the user for both x and y, casts them as inegers and saves them into their respective x and y variables. Then, the ```if``` statement compares x and y. If the condition of ```x < y``` is met, the print statement is executed.
- ```if``` statements use ```bool``` or boolen values (true or false) to decide whether or not to execute. If the statement ```x < y``` is true, the compiler will register it as ```true``` and execute the code.

---
### Control Flow, elif, and else
- Obviously, that first example does not cover all of the possible solutions for x and y. We should account for all possible variations in our code. So we modify it in the follow way:
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x < y:
    print("x is less than y")
if x > y:
    print("x is greater than y")
if x == y:
    print("x is equal to y")
```
- Now, we are providing a series of ```if``` statements. The ```if``` statements are evaluated in the order in which they appear in your code. "left to right... top to bottom."
- This flow of decisions is called "control flow."
- The logic of our script could be graphed as follows:
![](../../assets/images/flow1.png)
- However, it is painfully obvious to us that asking three consecutive quesions is not the best use of time. After all, not all three questions can have an outcome of ```True```.
- We can revise our script using ```elif``` to allow the program to make less decisions.
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
elif x == y:
    print("x is equal to y")
```
- In this control flow, the first ```if``` statement is evaluated. If this statement is found to be true, all the ```elif``` statements will not be run at all.
- Our code can be represented as follows:
![](../../assets/images/flow2.png)
- While your computer may not noteice a difference between the first instance and this revision. Consider how a much time a simple decision like this saves when running in an online data center performing billions or trillions of operations like this per day. 
- As effecent coders, it is our task to be mindful of the complexity of our operations and to midigate wasted steps (and time) where possible. Unneccessary complexity often leads to failed/unstable code. 
- There is one final improvement we can make to our program. Take note how logically ```elif x == y``` is not a necessary evaluation to run. After all, if logically x is not lesss than y AND x is not greater than y, x MUST be equal y.
- In this case, we can create a "catch-all," default outcome using an else statement. We can revise as follows:
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
else x == y:
    print("x is equal to y")
```
- Noticed when graphed, how the relative complexity of this program has decreased through our revision.
![](../../assets/images/flow3.png)

---
### Homework
#### "42", Wire Hanger, Meat Hook, Baseball Bat"

>“All right,” said the computer, and settled into silence again. The two men fidgeted. The tension was unbearable.
>“You’re really not going to like it,” observed Deep Thought.
>“Tell us!”
>“All right,” said Deep Thought. “The Answer to the Great Question…”
>“Yes…!”
>“Of Life, the Universe and Everything…” said Deep Thought.
>“Yes…!”
>“Is…” said Deep Thought, and paused.
>“Yes…!”
>“Is…”
>“Yes…!!!…?”
>“Forty-two,” said Deep Thought, with infinite majesty and calm.”
>— The Hitchhiker’s Guide to the Galaxy, Douglas Adams

In deep.py, implement a program that prompts the user for the answer to the Great Question of Life, the Universe and Everything, outputting Yes if the user inputs 42 or (case-insensitively) forty-two or forty two. Otherwise output No.