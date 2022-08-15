---
layout: default
title: 04 - Conjunctions, Lists, and Loops
nav_order: 5
nav_exclude: false
---
# 04 - Conjunctions, Lists, and Loops
### Lesson Outline:
- 03 - Conditionals and Control Flow Recap
- Homework Review
- Conjunction Junction... What's your function? (and/or)

---
### 03 - Conditionals and Control Flow Recap
- Breaking programs into functions makes them easier to understand and allows for part of your code to be reused across projects.
- Functions are defined using ```def``` with a name, parameters, and an indented block of code.
- It is important to remember that defining a function does not run it. One must call the function in order for it to run.
- ```if``` statements are often used to control whether or not a block of code is executed.
    - The first line opens with ```if``` and ends with a colon ```:```
    - The body of the ```if``` statement contains one or more statements that are indented (usually by 4 spaces)
- ```else``` is used when an ```if``` condition is *not* true.
    - ```else``` is most often used following an ```if``` statement.
    - ```else``` allows us to specify an alternative to execute when the ```if``` branch isn't taken.
- ```elif``` is used to specify additional tests.
    - One might want to provide several alternative choices, each with its own test.
    - Use ```elif``` and a condition to specify those additional/alternative choices.
    - These ```elif``` statements are always associated with an ```if``` statement.
    - If you are going to use ```elif``` in combination with an ```else``` statement, the ```else``` statement must be in the final position as it serves a "catch all" role.
- Conditionals are tested only once, and in the order they are written. So the order in which write the conditional tests matters. 
```python
grade = 85
if grade >= 70:
    print('Grade is C')
elif grade >= 80:
    print('Grade is B')
elif grade >= 90:
    print('Grade is A')
```
```bash
grade is c
```

---
### Homework Review
#### "42"

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

In ```deep.py```, implement a program that prompts the user for the answer to the Great Question of Life, the Universe and Everything, outputting Yes if the user inputs 42 or (case-insensitively) forty-two or forty two. Otherwise output No.


#### Homework Check
<script id="asciicast-0JIic0pR3pVZTqBqfuBnIygPJ" src="https://asciinema.org/a/0JIic0pR3pVZTqBqfuBnIygPJ.js" async data-autoplay="1" data-loop="1" data-rows="15" data-cols="90"></script>

---
### Conjunction Junction... What's your function? (and/or)
- ```or``` allows your program to decide between one or more alternative. For example, we could further edit our program as follows:
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x < y or x > y:
    print("x is not equal to y")
else:
    print("x is equal to y")
```
- Notice that the result of our program is the same, but the complexity is decreased and the effiency of our code is increased.
- It is, however, possible to avoid the use of ```or ``` altogether using other conditionals.
```python
x = int(input("What's x? "))
y = int(input("What's y? "))
if x != y:
    print("x is not equal to y")
else:
    print("x is equal to y")
```
- Similar to ```or```, ```and``` can be used within conditional statements.
- Let's look at an example called ```grade.py```
```python
score = int(input("Score: "))
if score >= 90 and score <= 100:
    print("Grade: A")
elif score >=80 and score < 90:
    print("Grade: B")
elif score >=70 and score < 80:
    print("Grade: C")
elif score >=60 and score < 70:
    print("Grade: D")
else:
    print("Grade: F")
```

---
### Lists
- Scenario: You have set up sensors to do temperature measurements in a storage room for rare books.
- Doing calculations or statistical operations with hundreds of individual variables called ```temperature_001```, ```temperature_002```, etc., would be very slow and unwieldy. Instead, you might want concatenate all of these values into a single variable that *lists* all of the values.
- Use a *list* to store many values together.
    - Contained within square brackets [...].
    - Values are separated by commas ```,```.
- A list contains a series of any data type: strings, ints, other lists. The items in a list are generically called "elements."
- Lists are "mutable" - meaning that they can be changed.
```python
temperatures = [17.3, 17.5, 17.7, 17.5, 17.6]
print('Temps:', temperatures)
```
- You can access the length of a string using ```len()```:
```python
temperatures = [17.3, 17.5, 17.7, 17.5, 17.6]
print('Temps:', temperatures)
print('Length:', len(temperatures))
```
- To access the individual elements of a list, you can simply call the position of the element in the list using square brackets. 
- *Remember, standard indexing makes the first element count from 0*
```python
temperatures = [17.3, 17.5, 17.7, 17.5, 17.6]
print('Temps:', temperatures)
print('Temp #2:', temperatures[2]) # note that this will print the value 17.7 from the provided list. 
```
- Remember that lists are "mutable" - meaning that they can be changed.
- Lists' values can be replaced by assigning to them.
- Use an index expression on the left of the assignment to replace a value.
```python
temperatures = [17.3, 17.5, 17.7, 17.5, 17.6]
temperatures[0] = 16.5
print('Temps:', temperatures) 
```
- Appending elements to a list lengthens is. 
- Use ```list_name.append``` to add items to the end of a list.
```python
temperatures = [17.3, 17.5, 16.5, 17.5, 17.6]
print('temperatures is initially:', temperatures)
temperatures.append(17.9)
temperatures.append(18.2)
print('temperatures has become:', temperatures)
```
- Note that ```append``` is a *method* of lists. It's like a function, except it is tired to particualr object.
- You can additionally use ```del``` to remove elements from a list entirely.
```python
temperatures = [17.3, 17.5, 16.5, 17.5, 17.6, 17.9, 18.2]
print('temperatures is initially:', temperatures)
del temperatures[2]
print('temperatures has become:', temperatures)
```
- ```del``` is not a function or a method so it is called first. Instead, this is what we refer to as a *statement* in the language, much like we have already seen with ```return``` and will see with other values soon. 

---
### *While* Loops
- In short, loops are a way to do something over and over again.
```python
print("meow")
print("meow")
print("meow")
```
- Running this code, you'll notice that the program meows three times. 
- In developing as a programmer, as we have discussed before, you want to conside how one could improve areas of one's code where one types the same thing over and over again. 
- Let's imagine that the goal of this program is to "meow" 500 times. It wouldn't be logical to type 500 instances of the expression ```print("meow")```.
- Loops enable you to creat a block of code that executes over and over again. 
- The ```while``` loop is nearly universal throughout all coding languages.
- This loop will repeat a block of code over and over again as long as the condition set remains true. Let's view an example.
```python
i = 3
while i != 0:
    print("meow")
```
- Notice how even though this code will execute ```print("meow")``` multiple times, it doesn't really fufill the conditions we imagined and it introduces an additional problem. This code will never stop running!
- In this case, the compiler is asking "does ```i``` not equal zero?". Becasue it never will, the program will never stop. When you get stuck in a loop that executes forever, you can press ```control-c``` on your keyboard to break out of the loop.
- To fix this loop that lasts forever, we can edit our code as follows:
```python
i = 3
while i != 0:
  print("meow")
  i = i - 1
```
- Notice that now our code executes without endlessly looping, reducing ```i``` by ```1``` for each "iteration" through the loop.
- Iteration has special significance within coding. By iteration, we mean one cycle through the loop. The first iteration however, is the 0th iteration. The second is the 1st iteration. In programming, we count starting with 0.
- Now we have seen all of the consitutate parts necessary to complete the task we were imaginaing. As a reminder, we wanted a program that would "meow" 500 times.
```python
i = 0
while i <= 500:
  print("meow")
  i = i + 1
```
### Homework
#### Challenging Ourselves. I'm sorry. Kinda...

>Using while loop and an if statement write a function named name_adder which appends all the elements in a list to a new list unless the element is an empty string: "".
- Start by using the code provided below:
```python
lst1=["Joe", "Sarah", "Mike", "Jess", "", "Matt", "", "Greg"]
#Type your code here.
def name_adder(list):





print(name_adder(lst1))
```

##### Homework Hints
- No need to convert the user's input to an ```int``` if you check for equality with ```"42"```, a ```str```, rather than ```42``` and ```int```!
- It's okay if your output or the user's wraps onto multiple lines.