# ECE 2112 PROGRAMMING ASSIGNMENT 1 - INTRODUCTION TO PYTHON PROGRAMMING
## Programmed By: Eddrid Gabriell Viloria, 2ECE-C
This is the repository for the first programming assignment for ECE 2112, Advanced Computer Programming and Algorithms. What you will see here is the .ipynb file of the assignment itself, alongside this README file. Please ignore the `Untitled.ipynb`, as it is merely a test file to make sure both Git and GitHub work as intended.  
**Objective:** The students should be able to solve the following programming problems using basic Python functions, operators, and string operations, and manipulate strings via indexing, slicing, and other built-in string methods. The students are also tasked to be able to learn and apply sequence unpacking to manipulate the elements of a list. Lastly, we should be able to construct simple Python functions that are able to return a specified result.

## Programming Problem A - Word Rotation Problem
* The programmer was tasked to create a function named `rotate_word()`. What this function should do is that it should be able to move the first character of the entire string to the very end of it. This should be done while preserving the original order of the rest of the string. Additionally, it should be able to preserve the capitalization of every character and accept non-empty strings.
* Indexing and concatenation were used in the making of this function.
* Characters from the second letter of the word up to the very last one are printed in the return command by using the command `text[1:]` (Python will assume to go to the very edge of the string on the side with respect to the colon inside the square brackets). This would then be followed by the command `text[0]`, which prints the first character of the string, connected to the rest of the output by the concatenation `+`.
The code shown below is everything put together for this function to work as intended:
```python
def rotate_word(text):
    return(text[1:] + text[0])

print(rotate_word("python"))
print(rotate_word("logic"))
print(rotate_word("Code"))
print(rotate_word("A"))
```
In addition, another example was created in a separate cell to further demonstrate the function itself, this time without the use of the print command.
```python
rotate_word("pneumonoultramicroscopicsilicovolcanoconiosis")
```
## Programming Problem B - Username Builder Problem
* The programmer was tasked with this problem to create a function named `make_username(first_name, last_name)`, which, as the name suggests, creates a username for the user according to their inputted first and last name.
* The function must turn the user's full name into this specified format: `first_name.last_name`. Any spaces in their name must be removed, and all letters must be in lowercase.
* `.lower()` was used in order to convert all letters into lowercase.
* `.replace()` was also used in order to remove/replace any spaces with no space.
Putting everything together results in this code, which defines the function itself. Examples have also been included in order to ensure that the code is fully functional:
```python
def make_username(first_name, last_name):
    fname = first_name.lower()
    surname = last_name.lower()
    return(fname.replace(" ","") + "." + surname.replace(" ",""))

print(make_username("Ada", "Lovelace"))
print(make_username("Alan", "Turing"))
print(make_username("Ana Maria", "De Leon"))
```
An additional example is also given in a separate cell after this:
```python
make_username("Eddrid Gabriell", "Viloria")
```
## Programming Problem C - Bookend Swap Problem
* The programmer was tasked with this problem to create a function named `swap bookends()`. This function would swap the positions of the first and last items when used on a given list.
* This function would use extended sequence unpacking, `first, *middle, last`. This is a way for the programmer to properly label such items to be the first item in the list, the last, or somewhere in between, no matter how long the list is.
* Lastly, the function would give a return value, with the last item taking the place of the first item as intended, while keeping the order of the items in between intact.
Putting all this together gives us our code and solution for this problem, alongside examples that use this function:
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]

print(swap_bookends([1, 2, 3, 4, 5, 6]))
print(swap_bookends(["red", "green", "blue"]))
print(swap_bookends([8, 3]))
```
An additional example is also given in a separate cell after this to further ensure that the function is fully functional.
```python
swap_bookends(["Chapter 1", "Chapter 2", "Chapter 3", "Chapter 4"])
```
## Versions
**Aug. 23, 2026**  
* Version 0.1  
    - Development of PA1 initiated.  
* Version 0.2  
    - `rotate_word(text)` function fully operational.  
* Version 0.3  
    - `make_username(first_name, last_name)` function fully operational.  
**Aug. 24, 2026**  
* Version 0.4  
    - `swap_bookends(item)` function fully operational.  
**Aug. 25, 2026**  
* Version 1.0  
    - Program fully released into GitHub.  
    - Input feature replaced with all the examples from the PDF file added into the program.  
**Aug. 27, 2026**
* Version 1.1  
   - `print()` used as a way to execute and display the examples in using the developed functions, further reducing the number of cells present in the program.
   -  Additional examples added in each programming problem  
* "Reverted" Version 1.1 - Result of technical difficulties in git push. Reverted back to the original Version 1.1 moments later.  
* Version 1.2  
        - Additional examples from the previous version were transferred to separate cells. This is in order to demonstrate that functions are fully operational even without the `print()` command.  
