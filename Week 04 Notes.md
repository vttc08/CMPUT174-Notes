## Lecture - Jan 30
Check Wing IDE notes for lecture coding examples
## Lecture - Feb 1
**Opening Files**
File need filename and file mode
```python
file = open(filename, filemode)
```
`file` is from the `TextIOWrapper` class
Using `with` will close the filestream automatically when the suite finish
```python
with open(filename, filemode) as file:
	text = file.read()
```
- read method will read from the file
- `file.read` reads everything as one string

**Reading**
Open the file in read mode and read lines
```python
file = open(filename, filemode)
for line in file:
	print(line) # read the file line by line
```
- `repr()` will see everything in a string including the `\n`
- the length of content in a file in python will be 1 higher because the file also contain `\n`
- `readline()` read a single line from the file
```python
file = open(filename, filemode)
text = file.readline()
text2 = file.readline() # it will read the second line of the file, the program knows the first line is read
```
- `readlines()` read all the lines at once as a list

**Writing**
```python
file = open(filename, 'w')
file.write("Hello world\n")
file.close
```
Using with clause:
```python
with open(filename, 'w') as file:
	file.write('text\n')
```

**Closing**
	- if not using with, need to close the file using `file.close()`

**File mode**
- read
- write
- append

**While Loop**
For loop has specific number of times (definitive iteration), while loop can be infinite (indefinite operation), it will be stopped until a condition is reached
```python
while True:
	print('true')
while False: # this loop never run because it's false
	print('false')
```
```python
while i < 3: # this code will keep running as long as i is less than 3
	i += 1
```

## Module Notes
**Evaluation** - the process of determining the value of an expression
- eg. result = 1 + 2 + 3
**Execution** - process of performing an action
- eg. print a function

For loop is when we know how many times the program will execute, while loop we don't know how many times a suite should be repeated. While is used when we need to loop until a condition is met.

**File IO**
- opening the file
- reading the content
- closing the file
 ```python
 file = open(filename, filemode)
 file.read()
 file.close()
 ```
The file has a class of `io.TextIOWrapper`

```python
with open(filename, 'r') as myfile:
	text = myfile.read() # with statement close file automatically
```

**Reading**
- `file.read()` will print out the entire content of the file including `\n` which wil return as `line1\nline2\n` when using the `repr()`
- `file.readline()` will get the first line content of a file and the next line depending on how many times `readline` is called
```python
file = open(filename, filemode)
text1 = file.readline()
text2 = file.readline()
```
- `file.readline()` will return all the lines in a file as a list, the list will contain a `\n` at the end 
- `line.strip()` for each line in `file.readline()` will remove the `\n` from the file
```python
with open('', 'r') as myfile:
	for line in myfile.readlines():
		line = line.strip() # return the lines without the trailing \n
```
```python
with open('canada.txt','r') as canada:
  for line in canada:
    print(line.strip()) # read it lines one at a time without creating a list first
```
- once the file has been closed, it won't be available to the program anymore

**Writing**
- in write mode, the file write and overwrite the entire file content
- in append mode, the file will continue writing after the last line
- writing by default does not include `\n`