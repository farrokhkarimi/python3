# # Headlines
- [Introduction](#--Introduction)
- [IDEs](#--IDEs)
- [Installation](#--Installation)
- [Package Management](#--Package-management)
- [Basic Syntax](#--Basic-Syntax)
- [Data Types](#--Data-Types)
- [Operators](#--Operators)
- [Decision Making](#--Decision-Making)
- [Loops](#--Loops)
- [Data & Times](#--Date-and-Times)
- [Functions](#--Functions)
- [Files](#--Files)
- [Exception Handling](#--Exception-Handling)
- [OOP](#--Object-Oriented)
- [numpy Library](#--numpy-Library)
- [matplotlib Library](#--matplotlib-Library)

# - Introduction
- Easy, Easy, Easy
- Interpreted
- Interactive
- Object-Oriented

# - IDEs
- [Default IDE](https://www.python.org/)
- [Spyder](https://www.spyder-ide.org/)
- [PyCharm](https://www.jetbrains.com/pycharm/)

# - Installation
- **Windows:** exe file from website
- **Linux:** `sudo apt install python3` in terminal for Debian based distributions
- **Mac:** mac file from website
- **[Colab](https://colab.research.google.com/notebook#create=true)**

# - Package management
- **```pip install <package_name>```**
- **```!pip insatll <package_name>```** **(on jupyter or Colab)**
- **```Conda install <package_name>```**
- **Installation from source**

# - Basic Syntax

### Identiation:
```python
if True:
   print ("Hello World!")
```
```
Hello World!
```

### Comments:
```python
# This is a comment!
```

### Multi line comments:
```python
'''
A paragraph is a series of sentences that are organized and coherent, and are all related to a single topic. Almost every piece of writing you do that is longer than a few sentences should be organized into paragraphs.
'''
```

### Assignment:
```python
a = A = b = 1
x, y, z = 10, 20, 'Salam!'
print(z)
```
Result:
```
Salam!
```

### input:
```python
input() # Read a string from standard input
```
Ex:
```python
input('Press Enter key to continue...')
```
Ex:
```python
a = input('Please insert a number:')
```

# - Data Types

## Numbers:
```python
n = 1
h = 0x1F # Hexa-decimal
print(h)
del(n) # delete n variable
print(n) # NameError: name 'n' is not defined
```
Result:
```
31 # Decimal
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-10-9994857361e0> in <module>
      2 print(n)
      3 del(n) # delete n variable
----> 4 print(n) # NameError: name 'n' is not defined

NameError: name 'n' is not defined
```

## String:
```python
s = 'Ali'
print(s[1]) # return the second letter (l)
s = s + ' Karimi'
print(s)
```
Result:
```
l
Ali Karimi
```
Ex:
```python
name = 'Farrokh'
city = 'Shahin-Shahr'
print('My name is {} from {} city.'.format(name, city))
```
Result:
```
My name is Farrokh from Shahin-Shahr city.
```

- **S.find(sub[, start[, end]]) -> int** # Return the lowest index in S where substring sub is found

Ex:
```python
print(name.find('r'))
```
Result:
```
2
```

- **S.split(sep=None, maxsplit=-1) -> list of strings** # Return a list of the words in S, using sep as the delimiter string.

Ex:
```python
print(city.split('-'))
```
Result:
```
['Shahin', 'Shahr']
```

- **S.replace(old, new[, count]) -> str** # Return a copy of S with all occurrences of substring old replaced by new.

Ex:
```
print(city.replace('-', ''))
```
Result:
```
ShahinShahr
```

## List:
```python
l = [1, 'Salam', 2.03] # list variables are editable
print(l[1]) # return the second item (index is from zero!)
l[2] = 13
print(l)
```
Result:
```
Salam
[1, 'Salam', 13]
```

- **len(obj)** # Return the number of items in a container.

Ex:
```python
print(len(l))
```
Result:
```
3
```

### Indexing and Slicing
- L[1]
- L[-1]
- L[1:]
- L[:1]

### methods
- **L.append(object) -> None** -- append object to end

Ex:
```python
plangs = ['C++', 'Java', 'Python']
plangs.append('C#')
print(plangs)
```
Result:
```
['C++', 'Java', 'Python', 'C#']
```
- **L.count(value) -> integer** -- return number of occurrences of value.
- **L.index(value, [start, [stop]]) -> integer** -- return first index of value.
- **L.insert(index, object)** -- insert object before index.
- **L.pop([index]) -> item** -- remove and return item at index (default last).
- **L.remove(value) -> None** -- remove first occurrence of value.
- **L.reverse()** -- reverse *IN PLACE*
- **L.sort(key=None, reverse=False) -> None** -- stable sort *IN PLACE*

## Tuple:
```python
t = (1, 'Salam', 2.03) # tuple variables are read-only
t[2] = 2 # TypeError: 'tuple' object does not support item assignment
```
Result:
```
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-13-ca1c96989ca8> in <module>
      1 t = (1, 'Salam', 2.03) # tuple variables are read-only
----> 2 t[2] = 2 # TypeError: 'tuple' object does not support item assignment

TypeError: 'tuple' object does not support item assignment
```

## Dictionary:
```python
d = {'Name': 'Ali', 'Code':1, 'Dept': 'Eng'}
d['test'] = 'test' # add a new key: value to the dictionary
print(d.keys()) # print all the keys
print(d.values()) # print all the values
```
Result:
```
dict_keys(['Name', 'Code', 'Dept', 'test'])
dict_values(['Ali', 1, 'Eng', 'test'])
```

### **type(object_or_variable)** # Return the object's type.

## Data Type Conversion
- **int(x [,base])** # Converts x to an integer. The base specifies the base if x is a string.
- **float(x)** # Converts x to a floating-point number.
- **complex(real [,imag])** # Creates a complex number.
- **str(x)** # Converts object x to a string representation.
- **eval(str)** # Evaluate the given source in the context of globals and locals.

Ex:
```python
f = 20; eval('f')
```
Result:
```
20
```

- **tuple(s)** # Converts s to a tuple.
- **list(s)** # Converts s to a list.
- **dict(d)** # Creates a dictionary. d must be a sequence of (key,value) tuples.
- **chr(x)** # Converts an integer to a character.
- **ord(x)** # Converts a single character to its integer value.
- **hex(x)** # Converts an integer to a hexadecimal string.
- **oct(x)** # Converts an integer to an octal string.

## Mathematical Functions (from math library)
- **min(x1, x2,...)** # With a single iterable argument, return its smallest item.
- **max(x1, x2,...)** # With a single iterable argument, return its biggest item.
- **round(x [,n])** # Round a number to a given precision in decimal digits (default 0 digits).
- **abs(x)** # Return the absolute value of the argument.
```python
import math
```
- **math.ceil(x)** # Return the ceiling of x as an Integral.
- **math.floor(x)** # Return the floor of x as an Integral.
- **math.exp(x)** # Return e raised to the power of x.
- **math.log(x)** # Return the logarithm of x to the given base.
- **math.log10(x)** # Return the base 10 logarithm of x.
- **math.pow(x, y)** # Return x**y (x to the power of y).
- **math.sqrt(x)** # Return the square root of x.

## Random Number Functions (from random library)
```python
import random
```
- **random.random()** # random() -> x in the interval [0, 1).
- **random.randrange ([start,] stop [,step])** # Choose a random item from range(start, stop[, step]).
- **random.choice(seq)** # Choose a random element from a non-empty sequence.

Ex:
```python
random.choice('Hello World')
```
Result:
```
'o'
```

## Mathematical Constants (from math library)
- **math.pi** # The mathematical constant pi.
- **math.e** # The mathematical constant e.

## Trigonometric Functions (from math library)
- **math.tan(x)** # Return the tangent of x (measured in radians).
- **math.atan(x)** # Return the arc tangent (measured in radians) of x.
- **math.atan2(y, x)** # Return the arc tangent (measured in radians) of y/x.
- **math.hypot(x, y)** # Return the Euclidean distance, sqrt(x*x + y*y).
- **math.degrees(x)** # Convert angle x from radians to degrees.
- **math.radians(x)** # Convert angle x from degrees to radians.

### dir function:
```python
import math
content = dir(math)
print(content)
```
Result:
```
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
```

# - Operators

### Arithmetic Operators:
```python
+
-
*
/
%
**
//
```

### Comparison Operators:
```python
==
!=
>
<
>=
<=
```

### Assignment Operators:
```python
=
+=
-=
*=
/=
%=
```

### Logical Operators:
```python
not
and, &
or,  |
xor, ^
```

### Membership Operators:
```python
in
not in
```

### Identity Operators:
```python
is
is not
```

- **id()** # Return the identity of an object

# - Decision Making

### if:
```
if expression:
   statement(s)
```

### if...else:
```
if expression:
   statement(s)

else:
   statement(s)
```

Ex:
```python
state = True
if state:
    print(True)
else:
    print(False)
```
Result:
```
True
```

### if...elif...else:
```
if expression1:
   statement(s)
elif expression2:
   statement(s)
elif expression3:
   statement(s)
else:
   statement(s)
```

### nested if:
```
if expression1:
   statement(s)
   if expression2:
      statement(s)
   elif expression3:
      statement(s)
   else
      statement(s)
elif expression4:
   statement(s)
else:
   statement(s)
```

# - Loops

### while:
```
while expression:
   statement(s)
```

### while...else:
```
while expression:
   statement(s)
else:
   statement(s)
```

Ex:
```python
while False:
    print(1)
else:
    print(0)
```
Result:
```
0
```

### for:
```
for iterating_var in sequence:
   statement(s)
```

- **range()** # Return an object that produces a sequence of integers from start (inclusive) to stop (exclusive) by step.

Ex:
```python
for i in range(5):
    print(i)
```
Result:
```
0
1
2
3
4
```

Ex:
```python
for l in 'Python':
    print(l)
```
Result:
```
P
y
t
h
o
n
```

### for...else:
```
for iterating_var in sequence:
   statement(s)
else:
   statement(s)
```
Ex:
```python
numbers = [11,33,55,39,55,75,37,21,23,41,13]

for num in numbers:
   if num%2 == 0:
      print ('the list contains an even number')
      break
else:
   print ('the list does not contain even number!')
```
Result:
```
the list does not contain even number!
```

### nested loop:
```
for iterating_var in sequence:
   for iterating_var in sequence:
      statements(s)
   statements(s)
```

### break:
Ex:
```python
for letter in 'Python': 
   if letter == 'h':
      break
   print (letter)
```
Result:
```
P
y
t
```

### continue:
Ex:
```python
for letter in 'Python':
   if letter == 'h':
      continue
   print (letter)
```
Result:
```
P
y
t
o
n
```

### pass:
Ex:
```python
for letter in 'Python': 
   if letter == 'h':
      pass
      print ('This is pass block')
   print (letter)
```
Result:
```
P
y
t
This is pass block
h
o
n
```

### **enumerate(iterable[, start]) -> iterator for index, value of iterable** # Return an enumerate object.
Ex:
```python
for index, value in enumerate("hello"):
    print(index, value)
```
Result:
```
0 h
1 e
2 l
3 l
4 o
```

# - Date and Times
```python
import time
```

Ex:
```python
print(time.time())
print(time.ctime())
```
Result:
```
1582059454.4040768
Wed Feb 19 00:27:34 2020
```
- **time.sleep** # Delay execution for a given number of seconds.  The argument may be a floating point number for subsecond precision.

Ex:
```python
tick = time.time()
time.sleep(3)
print(time.time() - tick)
```
Result:
```
3.003288507461548
```

# - Functions
```
def functionname( parameters ): # parameters can have default values
   "function_docstring"
   function_suite
   return [expression]
```

Ex:
```python
def func(name, state = 'Ok'):
    print('{} is {}.'.format(name, state))
    
print(func('Ali'))
```
Result:
```
Ali is Ok.
```

### Anonymous Functions:
```
lambda [arg1 [,arg2,.....argn]]:expression
```

Ex:
```python
sum = lambda arg1, arg2: arg1 + arg2
print ("Summation is:", sum(10, 20))
```
Result:
```
Summation is: 30
```

### import ... as
```
import modname as aliasname
```

### from...import
```
from modname import name1[, name2[, ... nameN]]
```

### from...import *
```
from modname import *
```

# - Files
- **Open(file_name [, access_mode][, buffering]) -> F** # Open file and return a stream.  Raise IOError upon failure.
- **F.name** # Returns name of the file.
- **F.mode** # Returns access mode with which file was opened.
- **F.write(str)** # Write string to stream.
- **F.read(size=-1)** # Read at most n characters from stream.
- **F.close()** # Flush and close the IO object.
- **F.closed** # Returns true if file is closed, false otherwise.

Ex:
```python
f = open("foo.txt", "w")
f.write("Python is a great language.\nIs not it?\n")
f.close()
```

Ex:
```python
with open("foo.txt") as f:
   print(f.read())
```
Result:
```
Python is a great language.
Is not it?
```

### os library:
```python
import os
```
- **os.getcwd()**
- **os.listdir()**
- **os.mkdir('newdir')**
- **os.chdir('newdir')**
- **os.rename(current_file_name, new_file_name)**
- **os.remove(file_name)**
- **os.rmdir('dirname')**


# - Exception Handling
```
try:
   statement(s)
   ......................
except:
   If there is any exception, then execute this statement(s)
   ......................
else:
   If there is no exception, then execute this statement(s)
finally:
   This would always be executed.
```

Ex:
```python
try:
    print('Start!')
    1 / 0
except:
    print('Error!')
else:
    print('Ok')
finally:
    print('Finish!')
```
Result:
```
Start!
Error!
Finish!
```

Ex:
```python
def func(var):
   try:
      return int(var)
   except ValueError as Argument:
      print (Argument)

print(func("xyz"))
```
Result:
```
invalid literal for int() with base 10: 'xyz'
```

# - Object Oriented
```
class ClassName:
   'Optional class documentation string'
   class_suite
```
Ex:
```python
class Employee:
   'Common base class for all employees'
   empCount = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.empCount += 1
   
   def displayCount(self):
     print ("Total Employee %d" % Employee.empCount)

   def displayEmployee(self):
      print ("Name : ", self.name,  ", Salary: ", self.salary)
        
#This would create first object of Employee class"
emp1 = Employee("Ali", 5000)
#This would create second object of Employee class"
emp2 = Employee("Sali", 2000)
emp1.displayEmployee()
emp2.displayEmployee()
print ("Total Employee %d" % Employee.empCount)
print ("Employee.__doc__:", Employee.__doc__)
print ("Employee.__name__:", Employee.__name__)
print ("Employee.__module__:", Employee.__module__)
print ("Employee.__bases__:", Employee.__bases__)
print ("Employee.__dict__:", Employee.__dict__ )
```
Result:
```
Name :  Ali , Salary:  5000
Name :  Sali , Salary:  2000
Total Employee 2
Employee.__doc__: Common base class for all employees
Employee.__name__: Employee
Employee.__module__: __main__
Employee.__bases__: (<class 'object'>,)
Employee.__dict__: {'__module__': '__main__', '__doc__': 'Common base class for all employees', 'empCount': 2, '__init__': <function Employee.__init__ at 0x7f1c40a076a8>, 'displayCount': <function Employee.displayCount at 0x7f1c40a078c8>, 'displayEmployee': <function Employee.displayEmployee at 0x7f1c40a07ae8>, '__dict__': <attribute '__dict__' of 'Employee' objects>, '__weakref__': <attribute '__weakref__' of 'Employee' objects>}
```

# - numpy Library
```python
import numpy as np
```
Ex:
```python
n1 = np.array([1, 2, 3])
n2 = np.array([[1, 2], [3, 4]])
print(n1, n1.shape)
print(n2, n2.shape)
```
Result:
```
[1 2 3] (3,)
[[1 2]
 [3 4]] (2, 2)
```
- **np.zeros(shape, dtype=float, order='C')** # Return a new array of given shape and type, filled with zeros.
- **np.ones(shape, dtype=None, order='C')** # Return a new array of given shape and type, filled with ones.
- **np.arange([start,] stop[, step,], dtype=None)** # Return evenly spaced values within a given interval.
- **np.asarray(a, dtype=None, order=None)** # Convert the input to an array.

Ex:
```python
l = [1, 2, 3]
n = np.asarray(l)
print(n.shape)
```
Result:
```
(3,)
```

- **N.flatten(order='C')** # Return a copy of the array collapsed into one dimension.
- **N.resahpe(shape, order='C')** # Returns an array containing the same data with a new shape.
- **np.resahpe(a, newshape, order='C')** # Gives a new shape to an array without changing its data.
- **np.append(arr, values, axis=None)** # Append values to the end of an array.
- **np.concatenate((a1, a2, ...), axis=0, out=None)** # Join a sequence of arrays along an existing axis.
- **np.stack(arrays, axis=0, out=None)** # Join a sequence of arrays along a new axis.
- **np.insert(arr, obj, values, axis=None)** # Insert values along the given axis before the given indices.

# - matplotlib Library
```python
import matplotlib.pyplot as plt
```
Ex:
```python
x = np.arange(0,10) 
y = 2 * x + 5
plt.title("Matplotlib demo") 
plt.xlabel("X axis label") 
plt.ylabel("Y axis label") 
plt.plot(x,y)#,'ob') 
plt.show()
```

Ex:
```python
x = np.arange(0, 3 * np.pi, 0.1) 
y = np.sin(x) 
plt.title("sine wave form") 
plt.plot(x, y) 
plt.show() 
```

Ex:
```python
x = np.arange(0, 3 * np.pi, 0.1) 
y_sin = np.sin(x) 
y_cos = np.cos(x)
plt.subplot(2, 1, 1) # first subplot
plt.plot(x, y_sin) 
plt.title('Sine')
plt.subplot(2, 1, 2) # second subplot
plt.plot(x, y_cos) 
plt.title('Cosine')
plt.show()
```

**Thanks**

Author: Farrokh Karimi  
Contact: [LinkedIn](https://www.linkedin.com/in/farrokhkarimi), [Instagram](https://www.instagram.com/farrokhkarimi)
