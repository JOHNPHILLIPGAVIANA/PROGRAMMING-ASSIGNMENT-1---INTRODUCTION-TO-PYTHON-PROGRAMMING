# PROGRAMMING ASSIGNMENT 1 - INTRODUCTION TO PYTHON PROGRAMMING
## Gaviana, John Phillip V.
## 2ECE-A
This repository contains the Python program and readme file for Programming Assignment 1 - Introduction to Python Programming.

# A. Word Rotation Problem
'''python
def rotate_word(txt):
    #Rotates a non-empty string by moving the first character to the end while the order of other characters remain.

    if not txt:
        return txt
    return txt[1:] + txt[0] #Moves the first character in to the end.

user_txt = input("Please enter a word: ") #User input
result = rotate_word(user_txt) #Call the function 
print("Rotate Word: ", result) #Output
'''
