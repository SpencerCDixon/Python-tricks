Python: a general purpose programming language that blends procedural,
functional, and object-oriented paradigms.

"good programmers know that code is written for the next human being who has to
read it in order to maintain or reuse it" - pg 25

.pyc stands for compiled .py source

### Run Time Order
source -> byte code -> PVM (Python Virtual Machine)

**Python Module**: Library of additional tools, like ruby gems.

Stream Redirection:
```python
python script1.py > saveit.txt
```
this will redirect output from script1 to the saveit.txt

* Running scripts in same python irb session: `from imp import reload` (expects
    name of already imported module)

**Module**: package of variable names, known as a _namespace_, and the names
within that package are called attributes. Attributes are variable names
attached to a specific object. Importers get access to all names assigned at the
top level of a modules file.

`dir(module_name)` will print all possible attributs available in a module

**Debugging**
You can run python with a `-i` in order to get interacive mode when the program
is done running.  You can then import `pdb` in order to use the post mordem
feature `pm()` to see what the last error was that got executed

In order to activate the pdb debugging system you use the command:
`pdb.set_trace()`

*  `up/down` to go up/down stack frame
*  `n` to go to next line
*  `c` to continue to next step trace
*  `s` step into the next operation (might go to function call or next line)

## Data Types
Creating a dictionary (hash):
{ "one": 1, "two": 2 }
OR
dict(one=1, two=2)

Python is both _dynamically_ typed and _strongly_ typed.  Once you create a
String object, it remains a string object, and you can only call methods on that
the String responds to.

**Number Types**:
* integers
* floating point
* complex
* decimals
* rationals (numerator/denominator)
* sets

Two ways to print objects: full-precision and user friendly
These will change something like: ` 6.283000000000000004` to `6.283`

Using `math`
```python
import math
math.pi
math.sqrt(some_numb)

import random
random.random()

random.choice([1,2,3,4])
```
**Strings**
They are 0-indexed like in ruby
```python
S = 'Spam'
S[0] #  => 'S'
```
numbers, strings, and tuples are immutable.  lists, dictionaries, and sets are
not.

To check what methods are available on an object use the `dir` command:
`dir` lists variables assigned in the caller's scope when called with no
argument.  If you pass an argument it will list all attributes available for
that object.

```ruby
s = "string"
dir(s)

# pass method names into help:

help(s.replace)
```

Multi-line strings can be made with triple `'` 

*  First string in a method call acts as a doc-string (aka documentation for that
    method)
*  instead of comments, you can have global strings for documentation

**Data Science**:
NumPy: acts as a primary container for data to be passed between algorithms.
Can interact with low level languages such as C or Fortran very well.

pandas: provides rich data structures and functions designed to make working
with strucutred data fast and easy.


To turn a connection result into an array: `list(result)`
