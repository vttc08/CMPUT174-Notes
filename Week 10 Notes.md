## Lecture - Mar 12 (online slides)
**Multi-dimensional Lists**
- represent matrix, tables, grids
- we use double subscription to access the exact value in a list
```python
[[1,2], # row 1
[3,4]] # row 2
mylist[0][1] # row 1, column 2
```
For loop can also be used to create 2D list, or to get values
- outer loop = rows
- inner loop = column
```python
for i in range(rows): # outer loop
	row = []
	for j in range(col): # inner loop
		row.append(your_object) # append columns in a row
	matrix.append(row) # append all the rows
```
Printing a 2D List
```python
for row in matrix:
	rows = ""
	for j in rows:
		rows += str(j) + " "
	print(rows) # print out rows on multiple lines consisting of columns
```
Using range function
```python
for i in range(len(matrix)):
	rows = ""
	for j in range(len(matrix[0])):
		rows += str(matrix[i][j]) + " "
	print(rows)
```

**Transposing a Matrix**
- for loop over column to get column index
	- for each column, for loop over rows
- this flip the order of row and column, append it to a list
```python
for j in range(len(matrix[0])):
	row = []
	for i in range(len(matrix)):
		row.append(matrix[i][j])
	matrix.append(row)
```
## Lecture - Mar 14
**Mutability Assignment**
When we assign a list `mylist = alist`, it if the same list object and it's mutable
- if we change one list `mylist[0]=0`, the other list will also change
As for tuples, `mytuple = atuple`, a new object is created
- same occurs with string, integers, float because these are not mutable

**Cloning List**
To clone a list, use subscription to create a new list
`alist = mylist[:]`
```python
mylist = alist -> True # content are the same
mylist is alist -> False # different objects in memory
```
- however, this does not work on multidimensional list
To clone a multi-dimensional list, need to use `deepcopy`
```python
from copy import deepcopy
alist = deepcopy(mylist)
```

## Module 7 Notes
Multidimension list is represented as a matrix.
The list can be changed without creating new objects.
**Aliasing** - two variables that refer to the same object in computer memory
- when we applying an operation to immutable object (eg. `a=a+1`), the alias is no longer bound to the same object
- when applying an operation on mutable object, the change will be reflected into all variables aliasing to that object

