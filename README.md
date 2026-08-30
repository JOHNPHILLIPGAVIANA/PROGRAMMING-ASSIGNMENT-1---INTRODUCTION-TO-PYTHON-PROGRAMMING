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
### 4. Input Gathering and Output Display `(input, rotate_word, print)`
**Purpose:** The final block manages the application workflow. The `input()` function retrieves text entered by the user and assigns it to `user_txt`. This variable is then passed to `rotate_word()`, and the returned result is displayed in the terminal using the `print()` function.

# B. Username Builder Problem
The python program below shows how basic strings methods and string concatenation are used in building a username.
## Python Program and Explanation
```python
def make_username(first_name, last_name):
    clean_first = first_name.lower().replace(" ", "") #Converts the case in to lowercase and removes spaces from both first and last names
    clean_last = last_name.lower().replace(" ", "") #Converts the case in to lowercase and removes spaces from both first and last names
    return f"{clean_first}.{clean_last}" #Joins names using period

first_name_input = input("Please enter first name: ") #User input
last_name_input = input("Please enter last name: ") #User input
username = make_username(first_name_input, last_name_input) #Executes the function
print("Processed username: ", username) #Prints the result
```

### 1. The `make_username(first_name, last_name)` Function
**Purpose:** This statement defines a modular function named `make_username` that accepts two parameters: `first_name` and `last_name`. Setting up the logic within a function ensures that name transformations can be reused across different inputs consistently.
### 2. 






















