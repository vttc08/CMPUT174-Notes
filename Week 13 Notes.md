## Lecture - Apr 2
**Class**
- a type in python
- has a property and behavior
**Object** - an instance of a class
- new object is created by calling a function that has the same name as the class
- objects created from a certain class will have similar properties
```python
circle_1 = Circle() # circle_1 is an instance of Circle class
```
There are type conversion functions, it create a new object when called
- eg. `list()` `str()`
Objects can have instance attributes which are defined in class
```python
circle_2 = Circle(20) # radius property
```
- the circle can have a radius attribute with value of 20
**Instance Attribute** - a variable/identifier that refers to a data object
- eg. radius is an attribute of circle class
- to refer to an attribute `circle_2.radius` where circle is the object and radius is the attribute
The variable `self` is bound to an object of type `Class`
```python
class Circle:
c1 = Circle()
self -> c1
```
**Method** - a function defined inside a class
```python
class Circle:
	def method(self, radius):
```
- method implement behavior or operations that can be performed on objects of the class
- first parameter is `self` is used to refer to the object which the method is called on
```python
str.lower() # str is the object, lower is the method of string
```

```python
class Circle:
	def __init__(self, theradius):
		self.radius = theradius # define attributes
	def method(self, parameter):
		return self.radius*2 # define methods
mycircle = Circle(radius)
mycircle.method()
```
`__init__` is used to initialize the instance attribute of the newly created class object
- `radius` is the `attribute` and `theradius` is a parameter that can be used
- arguments to the initializer have to be given to the `__init__` function to create the object, eg. radius
- `self` in the init method is used to instantiate the attribute
- the init is called when a object is created
- any argument given to a class is passed on as parameter to the init method
	- eg. `mycircle = Circle(radius)` pass the argument `radius` as `theradius` parameter in the init method, and `mycircle` is bound to `self`
	- then `self.radius` attribute in the init method is initialized with the `radius` value
`methods` implement the behavior of the object
- `self` is always needed to be the first parameter in every method
- `self` and its attributes can be referenced in a method as it is the class object which method is called on
- after `mycircle` is initialized with its attributed, a method can be called `mycircle.method()`
	- `mycircle` is bound to the parameter `self` is the method

## Lecture - April 4

**Class Representations**
```python
def __str__(self):
    # return str representation of class object
    return f'Rectangle {self.color}' # what is returned when it's printed
```
- string representation of a class object when the object is printed
```python
__str__
print(Myclass("red")) # will print red
without
print(Myclass("red")) # will print <__main__.Myclass object at 0x0000024CF8CA01C0>
```

```python
def __eq__(self, other):
	return self.attribute == other.attribute
```
- `eq` method allow comparison of object attribute using `==`
Normally even when 2 objects have all the same attributes, they are not equal
- `obj1 == obj2 # False` it compares the memory reference of the object
- when using the `eq` method, the comparison will return `True` when the attribute is same