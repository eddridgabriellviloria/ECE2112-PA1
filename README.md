# ECE 2112 PROGRAMMING ASSIGNMENT 1 - INTRODUCTION TO PYTHON PROGRAMMING
## Programmed By: Eddrid Gabriell Viloria, 2ECE-C

**Objective:** The students should be able to solve the following programming problems using basic Python functions, operators, and string operations, and manipulate strings via indexing, slicing, and other built-in string methods. The students are also tasked to be able to learn and apply sequence unpacking to manipulate the elements of a list. Lastly, we should be able to construct simple Python functions that are able to return a specified result.

## Programming Problem A - Word Rotation Problem
*Students were tasked to create a function named "rotate_word()". What this function should do is that it should be able to move the first character of the entire string to the very end of it. This should be done while preserving the original order of the rest of the string. Additionally, it should be able to preserve the capitalization of every character and accept non-empty strings.
The code shown below is the solution/code for this function to work as intended:
```python
def rotate_word(text):
    return(text[1:] + text[0])
