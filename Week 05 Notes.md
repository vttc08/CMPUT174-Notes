## Lecture - Feb 6
**Advantage of User Defined Functions**
- structure and organization
- reusing codes
- divide bigger problems into smaller problems

**UDF** is a type of compound statement
```python
def function():
	print("Do something")
function() # calling the function is the same as built-in functions
# we can reuse the function and call it many times
```

**Arguments** are used to send information to functions
**Parameters** are found in function definition and tell the program if a function need arguments
```python
def func(a,b): # function has 2 parameters a and b
	print(a+b)
func(1,2) # 1 and 2 are function arguments
```
Not all function need arguments and parameters, but args can simplify the code.

**Return Statement**
When a function need to return a value.
```python
def func(a,b):
	c = a + b
	return c # the value c is return from the function
	print(c)
```
`print(c)` won't be executed because it's after the return function
When a function returns nothing, it is a `None`
```python
def func(a,b):
	c = a + b
c = func(a,b)
print(c) # None
# print out None because the function is not returning anything
```

**Namespaces**
**Global** - identifier that are accessible throughout the code
**Local** - identifier that are only accessible within a function
- local namespace and global namespace is not the same

**Main Function**
Main is the driver part of the program, is the function to call first.

Immutable object must be recreated in a function, to access it the object must be returned
```python
def double(num):
	num = num * 2 # the num will be created as a new object
double(5) # nothing, because the new num object is not returned and the original num is immutable
```
Mutable object
```python
def double(alist):
	for i in range(len(alist)):
		alist[i] = alist[i] * 2
double(alist) # list will be doubled, list is mutable and it is changed in the function
```
```python
def listfunc(alist):
	alist = [] # the list function creates a new list
	alist.append(1) # will append if a new list is not created
listfunc(mylist) # it does not process my list because alist is newly created in the UDF and it's not returned
```

## Module Notes
In functions, the parameter of the function is bound to an argument if given
- the order of the arguments matters in a function
How function generalize the code
```python
def pause():
	print('******') # we can only print the *
def pause(symbol):
	print(symbol*10) # we can print anything we want given a symbol
```
`print()` is a function that doesn't return anything so assigning `a = print("hello")` would result in a being None. `len()` is a function that return a number.
The variable assigned to the function will be `None` unless if the function has a `return`

It is not recommended to bind a identifier to a function name
```python
input = "my input"
a = input("my input") # input is already assigned 'my input'
# str object is not callable
```

**Namespace**
Local: exist only in the function
Global: can be used anywhere
- global variable can also be used in functions 
- the same identifier can simultaneously exist in global and a functions local namespace
```python
name = 1
def func():
	name = 2
```

**Mutable and Immutable**
Immutable objects, a new object must be created.
- when modifying a immutable object in a function, a new object is local namespace, it needs to be returned
For Mutable objects such as lists, the content can be changed.
- a list in a python function will be modified directly, no new object is created and no need for return to access the new list
