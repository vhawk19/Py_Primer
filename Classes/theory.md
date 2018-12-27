**Authors:** Pranav Shridhar and Mohita Bipin

**Edits:** 

***

# Decorators

* A decorator is a function that takes another function and extends the behavior of the latter function without explicitly modifying it. 
* The function/method name is preceded by '@' symbol.
* Eg. @classmethod and @staticmethod are the standard methods used in classes.

Consider the following example* :
```python
def make_pretty(func):
    def inner():
        print("I got decorated")
        func()
    return inner

def ordinary():
    print("I am ordinary")
```
When you run the following codes in shell

```python
>>>ordinary()
I am ordinary

>>> # let's decorate this ordinary function
>>> pretty = make_pretty(ordinary)
>>> pretty()
I got decorated
I am ordinary
```

In the example shown above, make_pretty() is a decorator. In the assignment step, 

```python
pretty = make_pretty(ordinary)
```

The function ordinary() got decorated and the returned function was given the name pretty.

We can see that the decorator function added some new functionality to the original function. This is similar to packing a gift. The decorator acts as a wrapper. The nature of the object that got decorated (actual gift inside) does not alter. But now, it looks pretty (since it got decorated).

Generally, we decorate a function and reassign it as,

```
ordinary = make_pretty(ordinary)
```
This is a common construct and for this reason, Python has a syntax to simplify this.

We can use the @ symbol along with the name of the decorator function and place it above the definition of the function to be decorated. For example,

```python
@make_pretty
def ordinary():
    print("I am ordinary")
is equivalent to

def ordinary():
    print("I am ordinary")
ordinary = make_pretty(ordinary)
```


# Regular Methods, Class Methods and Static Methods

## Regular Methods
* They are plain functions written inside a class. They require an instance variable.
* The word 'self' is generally used in the naming of the first arguement which refers to the current instance.
* The statements written inside this affects a single instance/object presently in use.
* It requires no additional syntax.

Example :
```python
def Addition(self, a, b):  # 'a' and 'b' are  instance variables
    sum = a + b
    return sum
```

The above function return the sum of two variables held inside one instance.

## Class Methods

* They are methods/functions which require a class variable.
* The word 'cls' is generally used in the naming of the arguement which refers to the current class.
* The statements written inside this affects the entire class instances/objects.
* The decorator keyword '@classmethod' is used before the actual function.

Example :
```python
class Employee:

    raise_amount = 1  # class variable

    ...
    ...

    @classmethod
    def raise_salary(cls):
        raise_amount = 1.5
        return None
```

The above function upon calling changes the value of 'raise_amount' to 1.5 for all the instances.

## Static Methods

* They are methods/functions which do not require neither class variable nor instance variable. 
* The decorator keyword '@staticmethod' is used before the actual function.
* Static methods, much like class methods, are methods that are bound to a class rather than its object.
* They do not require a class instance creation. So, are not dependent on the state of the object.

Example :
```python
class Person: 
    def __init__(self, name, age): 
        self.name = name 
        self.age = age 
    
    @staticmethod
    def isAdult(age): 
            return age > 18
```


### Difference b/w classmethod and staticmethod

* Static method knows nothing about the class and just deals with the parameters.
* Class method works with the class since its parameter is always the class itself.



---
####References

* Example* for decorators taken from https://www.programiz.com/python-programming/decorator
