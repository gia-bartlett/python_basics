
### Data Types:
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
% Another way to say it is “X divided by Y with J remaining.” The result of % is the J part, or the remaining part.
```python
print('Hello world!')  # Hello world!
print(2+2)  # 4
print("2" + "2") # 22
print("Hello" + "World") # HelloWorld
print("Hello" + ", " + "World" + "!") # Hello, World!
```

## STRINGS:  
```python
txt = "Hello World!"
a = txt[0] # H
b = txt[2:5] # llo
c = txt.strip() # remove any whitespace at beginning or end
d = txt.upper() # convert to UPPERCASE
e = txt.lower() # convert to lowercase
f = txt.replace("H", "J") # Replace the character H with a J
g = txt.startswith("Hello") # determine if there is a substring at the start
h = txt.endswith("World!") # determine if there is a substring at the end
i = print(", ".join(["bacon", "eggs", "beans"])) # join list of strings with another string as separator
j = print("bacon eggs beans".split(", ")) # turning a string with a certain separator into a list

```
## NUMBERS:
```python
print(min(1, 2, 3, 4, 0, 2, 1)) # finds minimum of some numbers or a list
print(max([1, 4, 9, 2, 5, 6, 8])) # finds the maximum of some numbers or a list
print(abs(-99)) # finds the distance of a number from zero (its absolute value)
print(round(5.3768, 2)) # rounds a number to a certain number of decimal places (num, decimal places)
print(sum([1, 2, 3, 4, 5])) # finds the total of a list
```

### NONE:  
The None object is used to represent the absence of a value.  
It is similar to null in other programming languages.  
Like other "empty" values, such as 0, [] and the empty string, it is False when converted to a Boolean variable.
When entered at the Python console, it is displayed as the empty string.  
The None object is returned by any function that doesn't explicitly return anything else.  

 ```python
None == None
True
>>None
>>print(None)
# None

def some_func():
  print("Hi!")
# Hi!

var = some_func()
print(var)
# None
```

### VARIABLES:  
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
###STRING FORMATTING:  
To combine strings and non-strings, you can convert the non-strings to strings and add them to each other.  
String formatting provides a more powerful way to embed non-strings within strings.  
String formatting uses a string's format method to substitute a number of arguments in the string.  
```python
# string formatting
nums = [4, 5, 6]
msg = "Numbers: {0} {1} {2}". format(nums[0], nums[1], nums[2])
print(msg)
# Numbers: 4 5 6
```
Each argument of the format function is placed in the string at the corresponding position, which is determined using the curly braces { }.  
String formatting can also be done with named arguments.  
```python
a = "{x}, {y}".format(x=5, y=12)
print(a)
# 5, 12
```
Another way of formatting is the f method  
```python
name = "Eric"
age = 74
f"Hello, {name}. You are {age}."
# 'Hello, Eric. You are 74.'
```