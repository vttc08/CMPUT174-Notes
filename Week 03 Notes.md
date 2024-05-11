## Lecture  - Jan 23
**Tuples**
- tuples are similar to list but are not mutable
- (1,2,3)
**Dictionary**
- store data in key:value pairs which can be any object type
- keys are immutable and not 2 keys should be same
- dictionaries are mutable
- `{'key':'value', 'key 2','123'}`
- dictionaries are indexed by keys, and we access its value using keys
**Slicing**
```python
mylist = [1,2,3,4,5]
mylist[0:2] # 1,2 
```
- define where the index start and end using : 
- `:2` the list end at 2nd value (not index 2)
- `3:` the list start at index 3 and end at the end of the list
## Lecture  - Jan 25
If statement is a compound statement
```python
if temp > 25:
	print('')
	if humid:
		print("") # this is a nested if statement, humid will not get checked if temp is less than 25
```
```python
if temp <= 0: # once if true, the elif and else is not checked
    print("")
elif temp > 0 and temp <10:
    print("")
else:
    print("")```
- the if statement is evaluated first and has an order
```python
if mark > 60:
	print("D")
elif mark > 70:
	print("C") # this is semantic/logical error, if is evaluated first so a mark of 75 would get C because mark > 60
```
- nesting if statements and using and get the same result
- check the indentation of if/else statement to avoid logical error

**For Loops**
```python
for i in range(1,11): # start at 1 end at 10, 11 is not included
	# range is a function
    print(i) # loop through 1 to 10
for j in range(1,100,10): # print from 1 end at 99, increment by 10
for k in range(5): # it defaults 0 as stop at 4
```
- for loop can also traverse strings or lists
```python
mystr = "CMPUT174" # will print each letter of mystr on a separate line
mystr = [1,2,3,4,5] # will print each item in the list
for str in mystr:
    print(str) 
for i in range(len(mystr)): # len of list is 5, the range stop 5 so value of 0,1,2,3,4 will be in i, which is the correct index of the list
```
- `ord` print the ASCII integer code for a letter
## Module Notes
Compound statements are made from header and suite
`elif` only evaluate if the clauses (if or elif) before it is not true
`else` if all the if and elif are not true
Nested If Statement, only evaluated if the conditional statement that is nested in is true

**Strings**
- string character can be subscribed (accessed using str[1] or str[0:3] to access multiple objects)
- string can be joined or multiplied
- `len(mystr)` get the number of characters in a string
- `"string"` is a string while `string` is an identifier
- `'i' in 'hello'` is used to check if a character exist, in this case it's `False`
- string content cannot be changed using `str[1]='x'` because it's immutable
- string has methods that is only specific to string type such as `string.upper()` which convert everything to uppercase

**Lists and Tuples**
List and tuples do not hold the actual objects, but the references to these objects, it can be reference to object of same or different types
- both list and tuples can be accessed using subscription
- both can be joined or duplicated into a larger list/tuple
- `len(listortuple)` get the number of characters in a string
- `'in' in mylist` is used to check if `in` exists in list
- only list content can be changed
- lists and only list have append method, which add objects to a list
- only methods available for tuple is count and index
- `tuple.count` count number of occurrence of an object
- `tuple.index` return the index of the first occurrence of an object
List and tuples can also reference another list/tuple in itself
- e.g. `[123, 456, [1,2,3,4,5]]`

**Ranges**
`range(start, stop, steps)`
- the range stop at a number 1 less than the stop value
- range will default with stop as its first argument and in that case it starts with 0
- range can step in positive/negative increments but cannot be a float
- range objects can be accessed by subscription
- `50 in range(0,50)` can be used to check if an object is in range, in this case `False` because the range stop at 49
- range object is immutable, `range(0,50)[0] = 1` would result in error

**For Loop**
