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
### 2. Empty String Validation Clause (`if not txt`)
**Purpose:** The clause conditional check evaluates whether the provided string is empty. If an empty string is passed, the function immediately returns it without performing further operations, ensuring stability and preventing errors during slicing.
### 3. String Slicing and Rearrangement (`return txt[1:] + txt[0]`)
**Purpose:** The line performs the primary character rotation. The expression `txt[1:]` extracts a substring containing every character from the second position to the end, while `txt[0]` isolates the initial character. The + operator combines these two parts, appending the original first letter to the end of the remaining string.
### 4. Input Gathering and Output Display (`input`,`rotate_word`, `print`)
**Purpose:** The `input()` function retrieves text entered by the user and assigns it to `user_txt`. This variable is then passed to `rotate_word()`, and the returned result is displayed in the terminal using the `print()` function.

# B. Username Builder Problem
The Python Program below shows how basic strings methods and string concatenation are used in building a username.
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
**Purpose:** A function named `make_username` is defined to accept two parameters: `first_name` and `last_name`. Setting up the logic within a function ensures that name transformations can be reused across different inputs consistently.
### 2. String Normalization (`.lower().replace(" ", "")`)
**Purpose:** The lines process both name inputs to ensure standard formatting. Calling `.lower()` converts all uppercase letters to lowercase which a standard for most username generation, while `.replace(" ", "")` strips out any spaces within the text, preventing formatting inconsistencies in the generated username.
### 3. Username Formatting and Assembly (`return f"{clean_first}.{clean_last}"`)
**Purpose:** The line uses f-string formatting to merge the processed string variables. It constructs and returns a single string containing the cleaned first name and last name separated by a period.
### 4. Input Gathering and Output Display (`input`, `make_username`, `print`)
**Purpose:** The `input()` prompts collect the first and last names, which are passed into `make_username()`. The resulting formatted string is saved in username and printed to the console using `print()`.

# C. Bookend Swap Problem
The Python Program below unpacks a sequence and returns a new list in which the first and last elements have exchanged positions.
## Python Program and Explanation
```python
def swap_bookends(items):
    first, *middle, last = items #Unpacking through extended sequence unpacking
    return [last, *middle, first] #Returns the new list with the first and last swapped

#User input
user_input = input(
    "Please enter items (Minimum of two (2) items): "
)
 
items_input = user_input.split()
result = swap_bookends(items_input) #Executes the function
print("Result: ", result) #Prints the result
```

### 1. The `swap_bookends()` Function
**Purpose:** Defines a modular function named  `swap_bookends ` that accepts a sequence of elements as  `items `. Packaging this operation into a function allows list bookend swapping to be executed consistently across different inputs.
### 2. Extended Sequence Unpacking (`first`, `*middle`, `last = items`)
**Purpose:** The line separates the incoming sequence into three components. The variable `first` receives the initial item, `last` captures the final item, and the starred target `*middle` collects all remaining elements between them into a list.
### 3. Reconstruction and Return (`return [last, *middle, first]`)
**Purpose:** The statement builds and returns a new list featuring swapped endpoints. Placing `last` at index 0 and `first` at the end exchanges the bookends, while `*middle` unpacks the middle elements to preserve their original sequence.
### 4. Input Gathering and Output Display (`input`, `split`, `print`)
**Purpose:** The `input()` prompt captures the raw input string, `split()` converts space-separated words into a list of items, and `swap_bookends()` processes the list before `print()` displays the final output in the terminal.














