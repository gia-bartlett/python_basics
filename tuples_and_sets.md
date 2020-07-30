### TUPLES:  
Tuples are very similar to lists, except that they are immutable (they cannot be changed).  
Also, they are created using parentheses, rather than square brackets.  
You can access the values in the tuple with their index, just as you can with lists;  
Trying to reassign a value in a tuple causes a TypeError.  
If you want to change a tuple you must convert it into a list, change and then convert back.  
Like lists and dictionaries, tuples can be nested within each other.  

```python
words = ("bacon", "eggs", "sausages",)
print(words[0])
words[1] = "cheese"
# TypeError: 'tuple' object does not support item assignment
```

Tuples can be created without the parentheses, by just separating the values with commas.  
An empty tuple is created using an empty parenthesis pair.  
Tuples are faster than lists, but they cannot be changed.  


| Type       | Format                    | Brackets | Indexed | Mutable  | Ordered | Duplicates |
| :--------: | :-----------------------: | :------: | :-----: | :------: | :-----: | :--------: |
| List       | name = ["list1", "list2"] | []       | Yes     | Yes      | Yes     | Yes        |
| Dictionary | name = {"key" : "value"}  | {}       | Yes     | Yes      | No      | No         |
| Tuple      | name = ("list1", "list2") | ()       | Yes     | No       | Yes     | Yes        |
| Set        | name = {"list1", "list2"} | {}       | No      | Yes      | No      | No         |

[0] refers to first item (when reading left to right)  
[-1] refers to last item (when reading right to left)  
[2:5] starts at index 2 (included) end at index 5 (not included) 