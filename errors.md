### EXCEPTION HANDLING:  
Exceptions occur when something goes wrong, due to incorrect code or input. When an exception occurs, the program immediately stops.  
Different exceptions are raised for different reasons.  
Common exceptions:   
ZeroDivisionError (trying to divide something by 0);  
ImportError: an import fails;  
IndexError: a list is indexed with an out-of-range number;  
NameError: an unknown (undefined) variable is used;  
SyntaxError: the code can't be parsed properly;  
TypeError: a function is called on a value of an inappropriate type;  
ValueError: a function is called on a value of the correct type, but with an inappropriate value.  
KeyError: indexing a key that isn't part of the dictionary.   
MemoryError: trying to create a list in a very extensive range. 
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

###ASSERTION:  
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
