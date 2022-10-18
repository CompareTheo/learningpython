---
layout: default
title: 05 - Recap Lessons 1-4
nav_order: 6
nav_exclude: false
---
# 05 - Lessons 1-4 Recap Day
### Lesson Outline:

---
### Putting it all together - Review Lessions 1-4
#### Example One - 100 Years
- Create a program that asks the user to enter their name and their age. Print out a message addressed to the user that tells them the year that they will turn 100 years old. Correct responses will use f-strings to print the resulting output message.
```python
name = input("What's your name? ")
age = int(input("What is your age? "))
year = 2022 - age + 100
print(f"{name}, will be 100 years old in the year {year}")
```

---
#### Example Two - Working with Lists
- Take a list, say for example this one: [7,3,13,6,8,5,1,2,4,15,9,10,12,14,11]. Write a program that prints out all of the elements of the list that are less than 5. However, instad of printing the elemens one-by-one, make a new list that has all of the elements less than 5 from this list in it and print out this new list.
```python
numbers = [7,3,13,6,8,5,1,2,4,15,9,10,12,14,11]
underFive = []
for element in numbers:
    if element < 5:
        underFive.append(element)
print(numbers)
print(underFive)
```

---
#### Example Three - Sierra Together
- Given this list of sierra oclc numbers, [1060588404,1097465769,1242107496,1060588404,1289623505,1289623505,1097465769,1242107496] create a program that deduplicates these numbers into a clean list. Using a method discussed in previously, be sure to traverse the list and then append the first occurrence of the element to the new list, ignoring all duplicated elements. 
```python
sierra_list = [1060588404,1097465769,1242107496,1060588404,1289623505,1289623505,1097465769,1242107496]
deduplicated = []
for i in sierra_list:
    if i not in deduplicated:
        deduplicated.append(i)
print(f"The orignal list is {sierra_list}")
print(f"The list after removing duplicates: {deduplicated}")
```

---