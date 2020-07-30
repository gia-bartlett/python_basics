### LISTS:  
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
# Hello
# world
# !
```

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
# 0  
# [1, 2, 3]  
# 3  
```

Lists of lists are often used to represent 2D grids, as Python lacks the multidimensional arrays that would be used for this in other languages.  

Indexing out of the bounds of possible list values causes an IndexError.  
Some types, such as strings, can be indexed like lists.  
Indexing strings behaves as though you are indexing a list containing each character in the string.  
For other types, such as integers, indexing them isn't possible, and it causes a TypeError.  
```python
str = "Hello world!"
print(str[6])
# w
```

The item at a certain index in a list can be reassigned.  

```python
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums)
# [7, 7, 5, 7, 7] 
```

Lists can be added and multiplied in the same way as strings.  
Lists and strings are similar in many ways - strings can be thought of as lists of characters that can't be changed.  

```python
nums = [1, 2, 3]
print(nums + [4, 5, 6])
print(nums * 3)
# [1, 2, 3, 4, 5, 6]  
# [1, 2, 3, 1, 2, 3, 1, 2, 3]  
```

To check if an item is in a list, the in operator can be used.  
It returns True if the item occurs one or more times in the list, and False if it doesn't.  
The in operator is also used to determine whether or not a string is a substring of another string.  

```python
words = ["bacon", "egg", "beans", "sausage"]
print("bacon" in words)
print("egg" in words)
print("tomato" in words)
# True
# False
# True
```

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
# [1, 2, 3, 4]  

```
The insert method is similar to append, except that it allows you to insert a new item at any position in the list, as opposed to just at the end.  

```python
words = ["Python", "fun"]
index = 1
words.insert(index, "is")
print(words)
# ['Python', 'is', 'fun']  

```

To get the number of items in a list, you can use the len function.  
Unlike append, len is a normal function, rather than a method.  
This means it is written before the list it is being called on, without a dot.  

```python
nums = [1, 3, 5, 2, 4]
print(len(nums))
# 5
```

To change the value of an entry in the list you need to provide the position of the current value and the new value.  
```python
fruits = ["apple", "banana", "cherry"]
fruits[0] = "kiwi"
print(fruits)
# ["kiwi", "banana", "cherry"]
```

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
list.append(): Adds and item ot the end of a list  
list.insert(): Inserts an item in chosen position in a list  


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

### SLICING:  
List slices provide a more advanced way of retrieving values from a list.  
Basic list slicing involves indexing a list with two colon-separated integers.  
This returns a new list containing all the values in the old list between the indices.  
Slicing can also be done on tuples.

```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[2:6])
print(squares[3:8])
print(squares[0:1])
```
[4, 9, 16, 25]  
[9, 16, 25, 36, 49]  
[0]  

Like the arguments to range, the first index provided in a slice is included in the result, but the second isn't.  
If the first number in a slice is omitted, it is taken to be the start of the list.  
If the second number is omitted, it is taken to be the end.  
```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[:7])
print(squares[7:])
```
[0, 1, 4, 9, 16, 25, 36]  
[49, 64, 81]  

List slices can also have a third number, representing the step, to include only alternate values in the slice.  
```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[::2])
print(squares[2:8:3])
```
[2:8:3] will include elements starting from the 2nd index up to the 8th with a step of 3.  
[0, 4, 16, 36, 64]  
[4, 25]  
Negative values can be used in list slicing (and normal list indexing).  
When negative values are used for the first and second values in a slice (or a normal index), they count from the end of the list.  
```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[1:-1])
```
If a negative value is used for the step, the slice is done backwards.  
Using [::-1] as a slice is a common and idiomatic way to reverse a list.  
[1, 4, 9, 16, 25, 36, 49, 64]  
print(list[starting point: end point: step])  

#### LIST COMPREHENSIONS:  
List comprehensions are a useful way of quickly creating lists whose contents obey a simple rule.  
```python
# a list comprehension
cubes = [i**3 for i in range(5)]

print(cubes)
# [0, 1, 8, 27, 64]
```
A list comprehension can also contain an if statement to enforce a condition on values in the list.  
```python
evens=[i**2 for i in range(10) if i**2 % 2 == 0]

print(evens)
# [0, 4, 16, 36, 64]
```
Trying to create a list in a very extensive range will result in a MemoryError.  
This issue can be solved by generators.  

### FOR LOOPS:  
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

# hello!  
# hello!  
# hello!  
# hello!  
# hello! 
```
### LIST FUNCTIONS:
Often used in conditional statements, all and any take a list as an argument, and return True if all or any (respectively) of their arguments evaluate to True (and False otherwise).  
The function enumerate can be used to iterate through the values and indices of a list simultaneously.  
```python
nums = [55, 44, 33, 22, 11]

if all([i > 5 for i in nums]):
   print("All larger than 5")

if any([i % 2 == 0 for i in nums]):
   print("At least one is even")

for v in enumerate(nums):
   print(v)
# All larger than 5
# At least one is even
# (0, 55)
# (1, 44)
# (2, 33)
# (3, 22)
# (4, 11)
```
