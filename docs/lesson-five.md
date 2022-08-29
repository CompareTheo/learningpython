---
layout: default
title: 05 - Recap Lessons 1-4
nav_order: 6
nav_exclude: false
---
# 05 - Lessons 1-4 Recap Day
### Lesson Outline:
- Homework Review
- Q&A Time
- Working with external data
- WHH Example

---
### Putting it all together - Review Lessions 1-4
#### Functions
- We have discussed in detail the need for/use of functions in your code applications.
- Python has built in functions that we have used over and over again (ie. ```print()```, ```input()```) but we might want to make our own.
- Functions serve as reusable blocks of code that are great for performing the same tasks over and over again. (In our example today, you may want to have a function that removes all of the blank entries from a list.)
- A properly defined function consists of the following components.
  1. Keyword ```def``` that marks the start of the function header.
  2. A function name to uniquely identify the function. (Convention is all lowercase with an underscore to seperate words in the function name.)
  3. Parameters through which we pass values to a function. (These are optional.)
  4. A colon (:) to mark the end of the function header.
  5. One or more valid pythong statements that make up the function body. Statements must have the same indentation level (usually 4 spaces).
- Defining a function is often not very useful without a functional return statement.
- Return is a special keyword in python that allows the function to output the value of a variable produced within the function.
```python
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))
def square(n):
    return n * n
main()
```
#### IF statements
