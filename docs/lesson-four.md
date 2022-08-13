---
layout: default
title: 04 - More Conditionals and The Pythonic Way
nav_order: 5
nav_exclude: false
---
# 04 - More Conditionals and The Pythonic Way
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
- Doing calculations with a hundred variables called ```temperature_001```, ```temperature_002```, etc., would be very slow and unwieldy. Instead, you might want concatenate all of these values into a single variable that *lists* all of the values.
- Use a *list* to store many values together.
    - Contained within square brackets [...].
    - Values are separated by commas ```,```.
```python
temperatures = [17.3, 17.5, 17.7, 17.5, 17.6]
print('Temps:', temperatures)
```
