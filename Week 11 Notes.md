## Lecture - March 19
**Dictionaries**
Data structure, a set of key value pairs were key and values are objects
- when we store in dictionary, the pair is stored
- there is no particular order with dictionary (unlike list)
Dictionaries are indexed by their keys
- keys have to be unique
- keys are immutable (string, int, tuple but not lists)
The value in the dictionary can be any type (immutable or not)

Dictionaries are more efficient to search.
Parallel list is not efficient
- it takes longer to search a parallel list 
- cannot sort both lists
- modifying list is error-prone

`{}` is the syntax used to create a dictionary
```python
mydict['newvalue'] = 12345 # add a new value to the dictionary
```
`[]` subscription is used to get the value of a key, similar to lists
- `KeyError` occur when accessing a key that doesn't exist, similar to `IndexError` in lists
```python
dict = {"key": "value", "key2": 25}
mydict['Key'] # return the value
mydict.get('Key', 'Default Value')
# if no default is given and key does not exist, it will return None
```
- `get` method the value for key if it exists and the default value if it doesn't

## Lecture - March 21
`dict.items()` return an iterable pairs
```python
for key, value in mydict.items():
	print(key, value)
"Key1 1" # each key value pair in the dictionary
"Key2 2"
```
`keys` method return iterable object keys
```python
for key in mydict.keys():
	print(key) # can also be used to get value of the associated key
"Key1"
```
`values` method return iterable object values
```python
for value in mydict.values():
	print(value) # cannot use value to get keys
```

Values in a dictionary is mutable, can assign new value to a key
- old value is replaced with a new value since keys are unique

Deleting Items
`pop` method, similar to `get` method
```python
mydict.pop(key1, default="key not found") # delete key1 from mydict
# when calling the print function on mydict.pop, it will print out the value
# it will result in KeyError when the key is not found
```

`in` operator is used to check if a key exist in a dictionary
```python
mydict = {"key1":"value", "key2": 123}
key1 in mydict # check if key1 exist in dictionary
value in mydict # False, can't check values in dictionary
value in mydict.values() # True, this will check if a value exist in dictionary
```
