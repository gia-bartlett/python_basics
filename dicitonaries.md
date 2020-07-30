### DICTIONARIES:  
Dictionaries are data structures used to map arbitrary keys to values.  
Lists can be thought of as dictionaries with integer keys within a certain range.  
Dictionaries can be indexed in the same way as lists, using square brackets containing keys.  
Each element in a dictionary is represented by a key:value pair.  
Dictionaries are structured as follows --> name = {key:value, key:value}  
An empty dictionary is defined as {}.  
  
```python
ages = {"Dave": 24, "Mary": 42, "John": 58}
print(ages["Dave"])
print(ages["Mary"])
```
24  
42

```python
primary = {
  "red": [255, 0, 0], 
  "green": [0, 255, 0], 
  "blue": [0, 0, 255], 
}

print(primary["red"])
print(primary["yellow"])
```
[255, 0, 0]

KeyError: 'yellow

Only immutable objects can be used as keys to dictionaries.  
Immutable objects are those that can't be changed.  
So far, the only mutable objects you've come across are lists and dictionaries.  
```python
bad_dict = {
  [1, 2, 3]: "one two three", 
}
```
TypeError: unhashable type: 'list'  

Just like lists, dictionary keys can be assigned to different values.  
However, unlike lists, a new dictionary key can also be assigned a value, not just ones that already exist.  

```python
squares = {1: 1, 2: 4, 3: "error", 4: 16,}
squares[8] = 64
squares[3] = 9
print(squares)
# {1: 1, 2: 4, 3: 9, 4: 16, 8: 64}
```
To determine whether a key is in a dictionary, you can use in and not in, just as you can for a list.  

```python
nums = {
  1: "one",
  2: "two",
  3: "three",
}
print(1 in nums)
print("three" in nums)
print(4 not in nums)
```
True  
False  
True  

#### GET:  
A useful dictionary method is get. It does the same thing as indexing,  
but if the key is not found in the dictionary it returns another specified value instead ('None', by default).  

```python
pairs = {1: "apple",
  "orange": [2, 3, 4], 
  True: False, 
  None: "True",
}

print(pairs.get("orange"))
print(pairs.get(7))
print(pairs.get(12345, "not in dictionary"))
```
[2, 3, 4]  
None  
not in dictionary 