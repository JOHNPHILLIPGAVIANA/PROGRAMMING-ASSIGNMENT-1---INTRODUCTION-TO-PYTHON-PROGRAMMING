# PROGRAMMING ASSIGNMENT 1 - INTRODUCTION TO PYTHON PROGRAMMING
## Gaviana, John Phillip V.
## 2ECE-A
This repository contains the Python program and readme file for Programming Assignment 1 - Introduction to Python Programming.

# A. Word Rotation Problem
The Python Program below shows how a character of a string is interchanged in position while keeping all other remaining characters in to their respective orders.
## Python Program and Explanation
```python
def rotate_word(txt):
    #Rotates a non-empty string by moving the first character to the end while the order of other characters remain.

    if not txt:
        return txt
    return txt[1:] + txt[0] #Moves the first character in to the end.

user_txt = input("Please enter a word: ") #User input
result = rotate_word(user_txt) #Call the function 
print("Rotate Word: ", result) #Output
```
### 1. The `rotate_word` Function
**Purpose:** Defines a reusable modular unit that accepts a single argument `(txt)`, which represents the word provided for processing.
### 2. Empty String Validation Clause `(if not txt)`
**Purpose:** The clause conditional check evaluates whether the provided string is empty. If an empty string is passed, the function immediately returns it without performing further operations, ensuring stability and preventing errors during slicing.
### 3. String Slicing and Rearrangement `(return txt[1:] + txt[0])`
**Purpose:** This line performs the primary character rotation. The expression `txt[1:]` extracts a substring containing every character from the second position to the end, while `txt[0]` isolates the initial character. The + operator combines these two parts, appending the original first letter to the end of the remaining string.
