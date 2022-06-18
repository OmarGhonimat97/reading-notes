## List Comprehensions

List comprehension provides a better way in dealing with lists and performing different functionalities on them.

> Syntax

Three ingredients are necessary for a python list comprehension to work:
1. The expression we’d like to carry out.
2. The object that the expression will work on.
3. Finally, we need an iterable list of objects to build our new list from.

### Notes about Lists Comprehensions

- List comprehension methods are an elegant way to create and manage lists. 
- In Python, list comprehensions are a more compact way of creating lists. 
- More flexible than for loops, list comprehension is usually faster than other methods.

> Create a List with range()

Example: Creating a list with list comprehensions 
```
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
```
Output
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

> Create a List Using Loops and List Comprehension in Python

Using loops
```
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
```
Using list comprehension
```
# create a list using list comprehension
squares = [x**2 for x in range(10)]

print(squares)
```

> Multiplying Parts of a List

By taking advantage of list comprehensions, it’s possible to work on only part of a list. For instance, if you only wanted the even numbers in a given range, you could find them using a filter.

Adding a filter to the list comprehension allows for greater flexibility. By using filters, we can select certain items from the list, while excluding others. This is an advanced feature of lists in Python.

 > Show the first letter of each word using Python

```
# a list of the names of popular authors
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

# create an acronym from the first letter of the author's names
letters = [ name[0] for name in authors ]
print(letters)
```
List comprehensions can make solving issues involving strings much easier using simplified expressions. These methods can save time and precious lines of code.
```
# use list comprehension to print the letters in a string
letters = [ letter for letter in "20,000 Leagues Under The Sea"]

print(letters)
```

> Lower/Upper case converter using Python

Using list comprehension to loop through a string in Python, it’s possible to convert strings from lower case to upper case, and vice versa. 

Making use of Python’s ***lower()*** and ***upper()*** methods, we’ll use list comprehension to achieve this common task.

> Print numbers only from a given string

Taking advantage of Python’s ***isdigit()*** method, we can extract the phone number from the user data.

> Parsing a file using list comprehension

It’s also possible to read files in Python using list comprehension. 

Using list comprehension, we can iterate through the lines of text in the file and store their contents in a new list.

> Using functions in list comprehensions

Not only can we write our own functions with list comprehensions, but we can also add filters to better control the statements.
