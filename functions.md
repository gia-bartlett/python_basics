### FUNCTIONS:  
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
