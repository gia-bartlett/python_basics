## STATEMENTS:
Python uses indentation (white space at the beginning of a line) to delimit blocks of code. In Python indentation is mandatory; programs won't work without it.  

### IF:  
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
### ELSE:  
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
### BOOLEAN LOGIC:  
Boolean logic is used to make more complicated conditions for if statements that rely on more than one condition.  
Python's Boolean operators are and, or, and not.  
####A ND  
The and operator takes two arguments, and evaluates as True if, and only if, both of its arguments are True. Otherwise, it evaluates to False.  
#### OR   
The or operator also takes two arguments. It evaluates to True if either (or both) of its arguments are True, and False if both arguments are False.  
#### NOT  
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

### WHILE LOOPS:  
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
#### BREAK:  
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

#### CONTINUE:  
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