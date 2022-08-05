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
<script id="asciicast-0JIic0pR3pVZTqBqfuBnIygPJ" src="https://asciinema.org/a/0JIic0pR3pVZTqBqfuBnIygPJ" async data-autoplay="1" data-loop="1" data-speed="2" data-rows="4" data-cols="80"></script>

---
