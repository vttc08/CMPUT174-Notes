## Lecture March 5
Testing is not proof of correctness (can't identify all errors). It's a process of validating and verifying the program.
To test a program effectively
- detailed understanding of the program
- knowledge of testing technique
Testing cannot be done effectively.

**White Box Testing**
- logical, structural, program-based testing
- testing input and output of a function
- how the implementation is done

**Debug**
F5 - start debugging
F7 - run code line by line
F11 - debug line by line in VSCode
`print` is quick way to debug the code, to see the value of variable

**Unit Testing**
focus on the smallest unit that comprise a software system (functions)

**pytest**
python library that make small readable tests
`python -m pytest`

```python
if __name__ == '__main__':
	main()
```
When importing a function that has a main function, the main function will run, this makes it that the main function won't run when functions are imported.

**assert** is used to test a condition, if there is a problem, the code stops
```python
assert True == True # nothing happens
assert True == False # assertion error
```

## Lecture Mar 7
**Multidimensional List (Matrix)**
```python
matrix = [[1,2],[3,4]] # 2D list
matrix[0][0] # list at index 0, then index 0 of that list
```
- nested lists can be used to represent tables, matrix, tables
Row are represented by a list within the 2D list.
Columns are represented by items in each row (list).

**Accessing Nested For Loop**
```python
for i in range(len(matrix)):
	for j in range(len(matrix[i])):
		print(j) # get individual value of a matrix
```

## Module Notes - Testing
