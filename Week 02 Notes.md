## Lecture - Jan 16
**Statements**
Simple statements: simple instruction with typically one line of code.
```python
print("hello world")
```
Compound statement: multiple statements that depend on each other, can be made up of simple statements
```python
if True or False:
for, while, if: ..
```

**Tokenization**
Breaking down code into tokens, similar to words, punctuation and symbol

Identifiers: functions (built-in or imported, created by user), variables
- can begin with _ or letter (`_identifier`,`identifier`)
- cannot be a python keyword (import, True), since python is case sensitive Import and true can be used but not recommended
- cannot start with digit (123letters)
- cannot have operators(plus+minus), the interpreter will try to evaluate it as expression
- eg. int, print, input
Literal: an actual value for a data
- eg. string, float, int, bool literal ("123", 4, 5.5, "CMPUT")
Delimiter: 
- `, . ( ) =`
- **=** is NOT a operator but delimiter, it assign a value of a literal to identifier
Keywords: cannot be substituted
- is, in, True, False, and
Operators: refer to operation 
- //, /, %, +, ==
- // - division without remainder
- % give the remainder
- and or logical operation uses keyword instead
- subscription [] e.g. get a value from a list, array uses delimiter
```python
list=[1,2,value, "string"]
print(list[0]) # subscription, get the 1st number of a list (list start at 0)
```

Syntax Errors: e.g. missing quote, brackets

Newline: line break separating statements
```python
print(1)
print(2)
print("1\n2") #\n is newline token when we start a newline
print(1, end="") # suppress new line
```

Refer to the python file to check in class example.

## Lecture - Jan 18
**Identity** - unique and immutable, determined when the object is created
```python
a = 'hello'
b = 'hello'
print(id(a),id(b)) # the id of a and b are same because they have the same string
```
Immutable: cannot modify any of these objects once they are created
**Type** of an object determine the kinds of operations that can be performed (eg. str, int, bool, float)
- types are immutable (can't be changed), but can be converted from one type to another
- the input function only accepts tstring so an input of integer, if adding it together, it will produce string concatenation instead of math
- `str()` `int()`

**Value** of object determine the memory content of each particular object
- values may be mutable (list) or immutable (tuple) depending on type of object
 
**None** type - None object indicate the value is nothing
- function can either return a value or None
- e.g. print() doesn't return any value 
- Nonetype is a type for None

**Function Type**
**List Type** 
- list will start from 0, the last index of list is the size minus one
- [0,1,2,3]
```python
list = [1,2,3]
print(list[3])
```
- Index error, it's a runtime error that occurs when the program is executing, the list index is out of range, there is no index at 3
- `len(list)` will get the size of the list
- List is mutable, we can assign new value to a number in a list. Where as in string, if doing `mystr[2]=x` would get runtime error, string does not support item assignment; it only support re-assignment of entire string. `mystr='xxx'`
```python
list = [1,2,3]
list.append(4)
```
- list is an object and append is a method that is invoked on the "list" object
- methods are like functions but has to act on objects
- `object.method()` 
- when we use method e.g. `variable.upper()` we created a new object with a different ID

## Module Notes
**Expression Statements** are statements that can be evaluated to produce a value (an object)
**Atomic Statement** the smallest piece of code that cannot be broken down further
`>>> 1` or `>>> x`
**Function Calls** computation and operation that are commonly used in programs, it is defined as its own function
- eg. print function
**Subscription** select an element from list, string or tuple
- eg `mylist[1]` gets the second value from mylist
**Slicing** select a range of items from a sequence
```python
string[0:3] # tells python to start at 0 index s and stop at index 3 which is the fourth letter i, the result would be str
string[-1] # the splicing is backward, result is g
```
**Attribute Reference** it references functions and constants in a module
- eg. `math.pi` pi is a attribute of math module
**Unary Expression** adding operator to an expression eg. `+5` `not True`
**Binary Expression** connecting one expression to another eg. `10+10` `a * 3`

**Assignment Statement** give names to objects in memory
`identifier = value` the value is assignment to identifier 
**Import Statement** give access to other modules
```python
import time
from time import sleep
```



