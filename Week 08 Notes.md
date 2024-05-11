## Module 6 Part B Notes
UDF improve structure and organization of code
- separate into logical blocks, making it easier to understand and maintain
UDF allows for reusing and reducing codes
UDF allows for solution generalization
- sometimes codes can be specific cases of a more general solution
- it reduce the need for creating separate functions for similar tasks

**Testing**
Testing verify the program work as expected and meet the requirements
"Happy path" - programmers tend to stick to data that make their program work

**Unit Testing**
White Box - test the inside part of your code
Black Box - focus on what the code does and not how 
We can use assert function to write tests

**pytest Unit Tests**
Dummy test
```python
def test_always_passes():
    assert True
def test_always_fails():
    assert False
```
- `.` means the test passed
- `F` means the test failed
- other symbol represent test skipped or error
Writing test functions
```python
from python_file import myfunction # import the functions

def test_case_1():
	assert myfunction(input) == expected # check if the function is working as expected
```