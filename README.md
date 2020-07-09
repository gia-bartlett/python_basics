PYTHON BASICS:  
https://www.sololearn.com/Play/Python  


print("Hello World!") = print the statement in the brackets  
input("What is your name? ") = ask the user for an input

Comments are annotations to code used to make it easier to understand.  
They don't affect how code is run.  
In Python, a comment is created by inserting an octothorpe (otherwise known as a number sign or hash symbol: #). All text after it on that line is ignored.  
```python
x = 365
y = 7
# this is a comment

print(x % y) # find the remainder
# print (x // y)
# another comment
# this will print 1
```
Docstrings (documentation strings) serve a similar purpose to comments, as they are designed to explain code.   However, they are more specific and have a different syntax.  They are created by putting a multiline string containing an explanation of the function below the function's first line.  
```python
ef shout(word):
  """
  Print a word with an
  exclamation mark following it.
  """
  print(word + "!")
    
shout("halp")
# prints halp!
```

- strings are used for simple text (str) (putting numbers in quotes will make them str)
- integers are whole numbers (int)
- floats are decimal numbers (float)
- Boolean (True / False)

| operations               |     |
| ------------------------ | --- |  
| addition                 | +   | 
| subtraction              | -   | 
| multiplication           | *   | 
| division                 | /   | 
| exponention              | **  | 
| quotient                 | //  | 
| modulo                   | %   |
| x = x + 3 (x += 3)       | +=  |
| equals                   | =   |
| is equal to              | ==  |
| is not equal to          | !=  |
| greater than             | >   |
| less than                | <   |
| greater than or equal to | >=  |
| less than or equal to    | <=  |

Python does not use ++ as a short cut for +=  
Be careful not to confuse assignment (=) with comparison (==).  
Num1 is(=) 7  
Num2 is equal to(==) 3  
Python's order of operations is the same as that of normal mathematics:  
parentheses first, then exponentiation, then multiplication/division, and then addition/subtraction.

```python
print('Hello world!')  # Hello world!
print(2+2)  # 4
print("2" + "2") # 22
print("Hello" + "World") # HelloWorld
print("Hello" + ", " + "World" + "!") # Hello, World!
```

VARIABLES:  
A variable allows you to store a value by assigning it to a name, which can be used to refer to the value later in the program.  
Variables can use letter, numbers, and underscores but they cannot start with numbers 

```python
num1 = 7
num2 = 3
print(num1 + num2) # 10
print(num1 + "!") # 7!
del num1 # this will delete the variable
num3 = input("Enter a number: ") # create a variable with user input
7 > 5 # True
```

STATEMENTS:
Python uses indentation (white space at the beginning of a line) to delimit blocks of code. In Python indentation is mandatory; programs won't work without it.  

IF:  
You can use if statements to run code if a certain condition holds.  
If an expression evaluates to True, some statements are carried out.  Otherwise, they aren't carried out.

```python
if 10 > 5:  # colon at end of if
   print("10 greater than 5")

print("Program ended")
```
To perform more complex checks, if statements can be nested, one inside the other.  
This means that the inner if statement is the statement part of the outer one.  This is one way to see whether multiple conditions are satisfied.
```python
num = 12
if num > 5:
   print("Bigger than 5")
   if num <=47:
      print("Between 5 and 47")
# Bigger than 5
# Between 5 and 7
```
ELSE:  
An else statement follows an if statement, and contains code that is called when the if statement evaluates to False.  
```python
x = 4
if x == 5:
   print("Yes")
else:
   print("No")
# No
```
You can chain if and else statements to determine which option in a series of possibilities is true.
```python
num = 7
if num == 5:
  print("Number is 5")
else: 
  if num == 11:
    print("Number is 11")
  else:
    if num == 7:
      print("Number is 7")
    else: 
      print("Number isn't 5, 11 or 7")
# Number is 7
```
BOOLEAN LOGIC:  
Boolean logic is used to make more complicated conditions for if statements that rely on more than one condition.  
Python's Boolean operators are and, or, and not.  
AND  
The and operator takes two arguments, and evaluates as True if, and only if, both of its arguments are True. Otherwise, it evaluates to False.  
OR   
The or operator also takes two arguments. It evaluates to True if either (or both) of its arguments are True, and False if both arguments are False.  
NOT  
Unlike other operators we've seen so far, not only takes one argument, and inverts it.
The result of not True is False, and not False goes to True.
```python
1 == 1 and 2 == 2 # True
1 != 1 and 2 == 2 # False
2 < 1 and 3 >  6 # False
1 == 1 or 2 == 3 # True
1 != 1 or 2 == 2 # True
2 < 1 or 3 >  6 # False
not 1 == 1 # False
not 1 > 7 # True
```
Operator precedence is a very important concept in programming.   
It is an extension of the mathematical idea of order of operations (multiplication being performed before addition, etc.) to include other operators, such as those in Boolean logic.

<img src="https://api.sololearn.com/DownloadFile?id=3515">  

WHILE LOOPS:  
An if statement is run once if its condition evaluates to True, and never if it evaluates to False.  
A while statement is similar, except that it can be run more than once.  
The statements inside it are repeatedly executed, as long as the condition holds.  
Once it evaluates to False, the next section of code is executed.  
The code in the body of a while loop is executed repeatedly. This is called iteration.  
```python
i = 1
while i <=5:
   print(i)
   i = i + 1

print("Finished!")
```
1  
2  
3  
4  
5  
Finished!  

The infinite loop is a special kind of while loop; it never stops running. Its condition always remains True.
```python
while 1==1:
  print("In the loop") 
```
You can stop the program's execution by using the Ctrl-C shortcut or by closing the program.  
To end a while loop prematurely, the break statement can be used.  
When encountered inside a loop, the break statement causes the loop to finish immediately.  
BREAK:  
Using the break statement outside of a loop causes an error.  
```python
i = 0
while 1==1:
  print(i)
  i = i + 1
  if i >= 5:
    print("Breaking")
    break

print("Finished")
```
0  
1  
2  
3  
4  
Breaking  
Finished  

CONTINUE:  
Another statement that can be used within loops is continue.  
Unlike break, continue jumps back to the top of the loop, rather than stopping it.  
Basically, the continue statement stops the current iteration and continues with the next one.  
Using the continue statement outside of a loop causes an error.  
```python
i = 0
while True:
   i = i +1
   if i == 2:
      print("Skipping 2")
      continue
   if i == 5:
      print("Breaking")
      break
   print(i)

print("Finished")
```
1  
Skipping 2  
3  
4  
Breaking  
Finished  

LISTS:  
Lists are another type of object in Python.  
They are used to store an indexed list of items.  
A list is created using square brackets with commas separating items.  
The certain item in the list can be accessed by using its index in square brackets.  
The first list item's index is 0, rather than 1, as might be expected.  
```python
words = ["Hello", "world", "!"]
print(words[0])
print(words[1])
print(words[2])
```
Hello  
world  
!  

An empty list is created with an empty pair of square brackets. []  
Most of the time, a comma won't follow the last item in a list.  
However, it is perfectly valid to place one there.  
Typically, a list will contain items of a single item type, but it is also possible to include several different types.  
Lists can also be nested within other lists.  
```python
number = 3
things = ["string", 0, [1, 2, number], 4.56]
print(things[1])
print(things[2])
print(things[2][2])
```
0  
[1, 2, 3]  
3  
Lists of lists are often used to represent 2D grids, as Python lacks the multidimensional arrays that would be used for this in other languages.  

Indexing out of the bounds of possible list values causes an IndexError.  
Some types, such as strings, can be indexed like lists.  
Indexing strings behaves as though you are indexing a list containing each character in the string.  
For other types, such as integers, indexing them isn't possible, and it causes a TypeError.  
```python
str = "Hello world!"
print(str[6])
```
w  

The item at a certain index in a list can be reassigned.  

```python
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums)
```
[7, 7, 5, 7, 7]   

Lists can be added and multiplied in the same way as strings.  
Lists and strings are similar in many ways - strings can be thought of as lists of characters that can't be changed.  

```python
nums = [1, 2, 3]
print(nums + [4, 5, 6])
print(nums * 3)
```
[1, 2, 3, 4, 5, 6]  
[1, 2, 3, 1, 2, 3, 1, 2, 3]  

To check if an item is in a list, the in operator can be used.  
It returns True if the item occurs one or more times in the list, and False if it doesn't.  
The in operator is also used to determine whether or not a string is a substring of another string.  

```python
words = ["bacon", "egg", "beans", "sausage"]
print("bacon" in words)
print("egg" in words)
print("tomato" in words)
```
True  
True  
False  

To check if an item is not in a list, you can use the not operator in one of the following ways:  

```python
nums = [1, 2, 3]
print(not 4 in nums)
print(4 not in nums)
print(not 3 in nums)
print(3 not in nums)
```
True  
True  
False  
False  

Another way of altering lists is using the append method.  
This adds an item to the end of an existing list.  

```python
nums = [1, 2, 3]
nums.append(4)
print(nums)
```
[1, 2, 3, 4]  

To get the number of items in a list, you can use the len function.  
Unlike append, len is a normal function, rather than a method.  
This means it is written before the list it is being called on, without a dot.  

```python
nums = [1, 3, 5, 2, 4]
print(len(nums))
```
5  

The insert method is similar to append, except that it allows you to insert a new item at any position in the list, as opposed to just at the end.  

```python
words = ["Python", "fun"]
index = 1
words.insert(index, "is")
print(words)
```
['Python', 'is', 'fun']  

The index method finds the first occurrence of a list item and returns its index.  
If the item isn't in the list, it raises a ValueError.  

```python
letters = ['p', 'q', 'r', 's', 'p', 'u']
print(letters.index('r'))
print(letters.index('p'))
print(letters.index('z'))
```
2  
0  
ValueError: 'z' is not in list  

There are a few more useful functions and methods for lists.  
max(list): Returns the list item with the maximum value  
min(list): Returns the list item with minimum value  
list.count(obj): Returns a count of how many times an item occurs in a list  
list.remove(obj): Removes an object from a list  
list.reverse(): Reverses objects in a list  

The range function creates a sequential list of numbers.  
The code below generates a list containing all of the integers, up to 10.  
The call to list is necessary because range by itself creates a range object, and this must be converted to a list if you want to use it as one.  

```python
numbers = list(range(10))
print(numbers)
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]  

```python
nums = list(range(5))
print(nums[4])
```
The above code has a list of numbers:  
[0, 1, 2, 3, 4]  
The print will return 4  
4 is the 5th character in the list  
4 is the 5th index in the list  
4 is at index 4 in the list  
num [0] = 0  
num [1] = 1   
num [2] = 2  
num [3] = 3   
num [4] = 4  

If range is called with one argument, it produces an object with values from 0 to that argument.  
If it is called with two arguments, it produces values from the first to the second.  

```python
numbers = list(range(3, 8))
print(numbers)

print(range(20) == range(0, 20))
```
[3, 4, 5, 6, 7]  

True  

Range can have a third argument, which determines the interval of the sequence produced.  
This third argument must be an integer.  

```python
numbers = list(range(5, 20, 2))
print(numbers)
```
[5, 7, 9, 11, 13, 15, 17, 19]  

```python
list = [1, 1, 2, 3, 5, 8, 13]
print(list[4])
print(list[list[4]])
```
4  
8 (this one takes the inside answer and the index for the first list)  

FOR LOOPS:  
Iterating through a list using a while loop requires quite a lot of code, so Python provides the for loop as a shortcut that accomplishes the same thing.  

```python
words = ["hello", "world", "bacon", "eggs"]
for word in words:
  print(word + "!")
```
hello!  
world!  
bacon!  
eggs!  

The for loop is commonly used to repeat some code a certain number of times.  
This is done by combining for loops with range objects.  
You don't need to call list on the range object when it is used in a for loop, because it isn't being indexed, so a list isn't required.  

```python
for i in range(5):
  print("hello!")
```
hello!  
hello!  
hello!  
hello!  
hello!  

FUNCTIONS:  
Code reuse is a very important part of programming in any language.  
Increasing code size makes it harder to maintain.  
For a large programming project to be successful, it is essential to abide by the Don't Repeat Yourself, or DRY, principle.  
Bad, repetitive code is said to abide by the WET principle, which stands for Write Everything Twice, or We Enjoy Typing.  

Any statement that consists of a word followed by information in parentheses is a function call.  
The words in front of the parentheses are function names, and the comma-separated values inside the parentheses are function arguments.  
Python is filled with predefined functions:  
print()  
range()  
str()  
len()  

In addition to using pre-defined functions, you can create your own functions by using the def statement.  
The code block within every function starts with a colon (:) and is indented.  
You must define functions before they are called, in the same way that you must assign variables before using them.   
Here is an example of a function named my_func. It takes no arguments, and prints "bacon" three times.  
It is defined, and then called. The statements in the function are executed only when the function is called.  

```python
def my_func():  # defining the function
   print("bacon")  # the body of the function (what it does)
   print("bacon")
   print("bacon")

my_func()  # calling the function
```
bacon  
bacon  
bacon  

Functions take arguments which are defined within the parentheses  
You can also define functions with more than one argument; separate them with commas.

```python
def print_sum(x, y):
   print(x + y)

print_sum(5, 8)
```
13  

Function arguments can be used as variables inside the function definition.  
However, they cannot be referenced outside of the function's definition.  
This also applies to other variables created inside a function.  
Technically, parameters are the variables in a function definition, and arguments are the values put into parameters when functions are called.  

```python
def function(variable):
   variable += 1
   print(variable)

function(7)  # this will print 8
print(variable)  # this will print a NameError name 'variable' is not defined
```
Certain functions, such as int() or str(), return a value that can be used later.   
To do this for your defined functions, you can use the return statement.  

```python
def max(x, y):
    if x >=y:
        return x
    else:
        return y
        
print(max(4, 7))
z = max(8, 5)
print(z)
```
7  
8  

Once you return a value from a function, it immediately stops being executed. Any code after the return statement will never happen.  

```python
def add_numbers(x, y):
  total = x + y
  return total
  print("This won't be printed")

print(add_numbers(4, 5))
```
9  

Although they are created differently from normal variables, functions are just like any other kind of value.  
They can be assigned and reassigned to variables, and later referenced by those names.  

```python
def multiply(x, y):
   return x * y

a = 4
b = 7
operation = multiply  # assigning the function multiply to the variable operation
print(operation(a, b))  # the name operation is used to call the function
```
28  

Functions can also be used as arguments of other functions.  As you can see, the function do_twice takes a function as its argument and calls it in its body.  

```python
def add(x, y):
  return x + y

def do_twice(func, x, y):
  return func(func(x, y), func(x, y))

a = 5
b = 10

print(do_twice(add, a, b))
```
30  

Modules are pieces of code that other people have written to fulfill common tasks, such as generating random numbers, performing mathematical operations, etc.  
The basic way to use a module is to add import module_name at the top of your code, and then using module_name.var to access functions and values with the name var in the module.  

```python
import random

for i in range(5):
   value = random.randint(1, 6)
   print(value)
```
The code uses the randint function defined in the random module to print 5 random numbers in the range 1 to 6.  
2  
3  
6  
5  
4  

There is another kind of import that can be used if you only need certain functions from a module.  
These take the form from module_name import var, and then var can be used as if it were defined normally in your code.  

```python
from math import pi

print(pi)
```
3.141592653589793  

(*) imports all objects from a module. For example: from math import *  
Use a comma separated list to import multiple objects, ie. from math import pi, sqrt  
This is generally discouraged, as it confuses variables in your code with variables in the external module.  

You can import a module or object under a different name using the as keyword.  
This is mainly used when a module or object has a long or confusing name.  

There are three main types of modules in Python, those you write yourself, those you install from external sources, and those that are preinstalled with Python.  
The last type is called the standard library, and contains many useful modules.  
Some of the standard library's useful modules include string, re, datetime, math, random, os, multiprocessing, subprocess, socket, email, json, doctest, unittest, pdb, argparse and sys.  

Tasks that can be done by the standard library include string parsing, data serialization, testing, debugging and manipulating dates, emails, command line arguments, and much more!  

EXCEPTION HANDLING:  
Exceptions occur when something goes wrong, due to incorrect code or input. When an exception occurs, the program immediately stops.  
Different exceptions are raised for different reasons. Common exceptions:   
ZeroDivisionError (trying to divide something by 0);  
ImportError: an import fails;  
IndexError: a list is indexed with an out-of-range number;  
NameError: an unknown (undefined) variable is used;  
SyntaxError: the code can't be parsed properly;  
TypeError: a function is called on a value of an inappropriate type;  
ValueError: a function is called on a value of the correct type, but with an inappropriate value.  
Python has several other built-in exceptions, such as OSError.  
Third-party libraries also often define their own exceptions.  

```python
num1 = 7
num2 = 0
print(num1/num2)
```
ZeroDivisionError: division by zero  

To handle exceptions, and to call code when an exception occurs, you can use a try/except statement.  
The try block contains code that might throw an exception.  
If that exception occurs, the code in the try block stops being executed, and the code in the except block is run.  
If no error occurs, the code in the except block doesn't run.  

```python
try:
   num1 = 7
   num2 = 0
   print (num1 / num2)
   print("Done calculation")
except ZeroDivisionError:
   print("An error occurred")
   print("due to zero division")
```
An error occurred  
due to zero division  

A try statement can have multiple different except blocks to handle different exceptions.  
Multiple exceptions can also be put into a single except block using parentheses, to have the except block handle all of them.  

```python
try:
   variable = 10
   print(variable + "hello")
   print(variable / 2)
except ZeroDivisionError:
   print("Divided by zero")
except (ValueError, TypeError):
   print("Error occurred")
```
Error occurred  

An except statement without any exception specified will catch all errors.  
These should be used sparingly, as they can catch unexpected errors and hide programming mistakes.  
Exception handling is particularly useful when dealing with user input.  

```python
try:
   word = "spam"
   print(word / 0)
except:
   print("An error occurred")
```
An error occurred  

To ensure some code runs no matter what errors occur, you can use a finally statement.  
The finally statement is placed at the bottom of a try/except statement.  
Code within a finally statement always runs after execution of the code in the try, and possibly in the except, blocks.  

```python
try:
   print("Hello")
   print(1 / 0)
except ZeroDivisionError:
   print("Divided by zero")
finally:
   print("This code will run no matter what")
```
Hello  
Divided by zero  
This code will run no matter what  

Code in a finally statement even runs if an uncaught exception occurs in one of the preceding blocks.  

```python
try:
   print(1)
   print(10 / 0)
except ZeroDivisionError:
   print(unknown_var)
finally:
   print("This is executed last")
```
1  
This is executed last  
ZeroDivisionError: division by zero  
During handling of the above exception, another exception occurred:  
NameError: name 'unknown_var' is not defined  

You can raise exceptions by using the raise statement.  
You need to specify the type of the exception raised.  

```python
print(1)
raise ValueError
print(2)
```
1  
ValueError  

Exceptions can be raised with arguments that give detail about them.  

```python
name = "123"
raise NameError("Invalid name!")
```
NameError: Invalid name!  

In except blocks, the raise statement can be used without arguments to re-raise whatever exception occurred.  

```python
try:
   num = 5 / 0
except:
   print("An error occurred")
   raise
```
An error occurred  
ZeroDivisionError: division by zero  

ASSERTION:  
An assertion is a sanity-check that you can turn on or turn off when you have finished testing the program.  
An expression is tested, and if the result comes up false, an exception is raised.  
Assertions are carried out through use of the assert statement.  
Programmers often place assertions at the start of a function to check for valid input, and after a function call to check for valid output.  

```python
print(1)
assert 2 + 2 == 4
print(2)
assert 1 + 1 == 3
print(3)
```
1  
2  
AssertionError  

The assert can take a second argument that is passed to the AssertionError raised if the assertion fails.  
AssertionError exceptions can be caught and handled like any other exception using the try-except statement, but if not handled, this type of exception will terminate the program.  

```python
temp = -10
assert (temp >= 0), "Colder than absolute zero!"
```
AssertionError: Colder than absolute zero!  

FILES: 
Reading files:   
You can use Python to read and write the contents of files.  
Text files are the easiest to manipulate. Before a file can be edited, it must be opened, using the open function.  
The argument of the open function is the path to the file.  
If the file is in the current working directory of the program, you can specify only its name.  

```python
myfile = open("filename.txt")
```
You can specify the mode used to open a file by applying a second argument to the open function.  
Sending "r" means open in read mode, which is the default.  
Sending "w" means write mode, for rewriting the contents of a file.  
Sending "a" means append mode, for adding new content to the end of the file.  
Sending "b" means binary mode, for reading individual bits.
You can use the + sign with each of the modes above to give them extra access to files.   
For example, r+ opens the file for both reading and writing.  

```python
# write mode
open("filename.txt", "w")

# read mode
open("filename.txt", "r")
open("filename.txt")

# binary write mode
open("filename.txt", "wb")
```
Once a file has been opened and used, you should close it.  
This is done with the close method of the file object = .close().  
This is only necessary when using open()  

```python
file = open("filename.txt", "w")
# do stuff to the file
file.close()
```
The contents of a file that has been opened in text mode can be read using the read method.  

```python
file = open("filename.txt", "r")
cont = file.read()
print(cont)
file.close()
# This will print all of the contents of the file "filename.txt".
```
To read only a certain amount of a file, you can provide a number as an argument to the read function.  
This determines the number of bytes that should be read.  
You can make more calls to read on the same file object to read more of the file byte by byte.  
With no argument, read returns the rest of the file.  
Just like passing no arguments, negative values will return the entire contents.  

```python
file = open("filename.txt", "r")
print(file.read(16))
print(file.read(4))
print(file.read(4))
print(file.read())
file.close()
```
After all contents in a file have been read, any attempts to read further from that file will return an empty string, because you are trying to read from the end of the file.  

```python
file = open("filename.txt", "r")
file.read()
print("Re-reading")
print(file.read())
print("Finished")
file.close()
```
Re-reading  
Finished  

To retrieve each line in a file, you can use the readlines method to return a list in which each element is a line in the file.  
```python
file = open("filename.txt", "r")
print(file.readlines())
file.close()
# ['Line 1 text \n', 'Line 2 text \n', 'Line 3 text']
```
You can also use a for loop to iterate through the lines in the file:  
```python
file = open("filename.txt", "r")

for line in file:
    print(line)

file.close() 
```
Line 1 text  

Line 2 text 
 
Line 3 text  

In this output, the lines are separated by blank lines, as the print function automatically adds a new line at the end of its output.  

Writing files:  
To write to files you use the write method, which writes a string to the file.  
The "w" mode will create a file, if it does not already exist.  

```python
file = open("newfile.txt", "w")
file.write("This has been written to a file")
file.close()

file = open("newfile.txt", "r")
print(file.read())
file.close()
```
This has been written to a file  

When a file is opened in write mode, the file's existing content is deleted.  

```python
file = open("newfile.txt", "r")
print("Reading initial contents")
print(file.read())
print("Finished")
file.close()

file = open("newfile.txt", "w")
file.write("Some new text")
file.close()

file = open("newfile.txt", "r")
print("Reading new contents")
print(file.read())
print("Finished")
file.close()
```
Reading initial contents  
some initial text  
Finished  
Reading new contents  
Some new text  
Finished  

The write method returns the number of bytes written to a file, if successful.  
To write something other than a string, it needs to be converted to a string first.  

```python
msg = "Hello world!"
file = open("newfile.txt", "w")
amount_written = file.write(msg)
print(amount_written)
file.close()
# 12
```
It is good practice to avoid wasting resources by making sure that files are always closed after they have been used.  
One way of doing this is to use try and finally.  
This ensures that the file is always closed, even if an error occurs.  

```python
try:
   f = open("filename.txt")
   print(f.read())
finally:
   f.close()
```
An alternative way of doing this is using with statements.  
This creates a temporary variable (often called f), which is only accessible in the indented block of the with statement.  
The file is automatically closed at the end of the with statement, even if exceptions occur within it.  

```python
with open("filename.txt") as f:
   print(f.read())
```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```
```python

```










