## Lecture - March 26
Check eClass for dictionary practice problems.

**JSON**
- a standard data format used for accessing API
- string formatted like a dictionary
Working with json in python
- json can be a dictionary or a list of dictionaries
```python
import json
mydict = json.loads(myjson) # json to dict
myjson = json.dumps(mydict) # dict to json
```
- `pprint` function will format the json
