**Author(s):  Mohita Liza Bipin, Pranav Shridhar**

**Editor(s): S Sandeep Pillai** 

# Classes and Instances


* A class defines a set of attributes for an object and an object is an instance of a class.

* Attributes include data members and methods.

* Methods are essentially functions defined within a class and data members are variables which are also defined within a class.


Yes, this seems a little complicated but it really isn't. Here's a simple analogy to help understand better:

A class is very similar to a basic chocolate cake recipe. It has all the ingredients (data) and the instructions (methods) to bake a cake. The object here is the cake.

Many objects can be made from a class and these objects can also be called instances.
This process is called instantiation.

Now that the definitions are out of the way we'll be taking a closer look at class and instances.

## Classes

### Defining a Class

To define a class use the class keyword followed by the class name.

```python

class Potato:
```

A local namespace containing the attributes is created when the class is defined where all attributes are defined.

###  Docstrings

Now looking at the class 'Potato' not a lot can be figured out about what exactly this class is for.
That is where docstrings come in handy.

Docstrings give anyone reading the code a heads up on what the class is used for.

```python
class example:
    '''This is a docstring'''  # -> Text enclosed by triple quotes. Explains the purpose of the class (when you hover over it in the text editor).
```


Now lets try applying this to our previous example, Potato.

```python
class Potato:
    '''This class is a template of different types of potatoes'''
```

To access a docstring use the syntax:

``` classname.__doc__```

```python
print(Potato.__doc__)
```

So this will print the docstring of Potato and the output will be

```This class is a template of different types of potatoes```


## Attributes


As we saw earlier attributes are both data members and methods so now we're going to add some attributes to Potato

```python
class Potato:
    '''This class is a template of different types of potatoes'''


    def info(self,kind):        # self? whats that!?
       self.kind = kind
```

'info' is an example of a method and 'kind' is a data member (attribute) describing the type of potato.

*'self'* is a parameter as whenever a method is called the instance as a whole is passed automatically as the first parameter.


### Q: WAIT WAIT WAIT WAIT, WHAT IS THIS `SELF` KEYWORD??? 

If you're like me, having learned C++ and coming over to python, you might be utterly confused with the reason python uses the `self` keyword. Infact, **`self` is not a keyword, you can use any word you like!** 


So in short, the `self` object is used to denote an `instance` variable, and its unique to that particular object of the class, not EVERY object of the class.

Consider the code below:

```python3

class A():
    x=3

class B():
    def __init__(self):
        self.x=3
        
```
Here is an important distinction:

A.x is a class variable, and will be **shared across all instances of A**, unless specifically overridden within an instance.
B.x is an instance variable, and **each instance of B has its own version of it.**


## Instances

### Creating an instance

An instance can be defined as follows

```instance_name = class_name() ```

A new instance called 'instance_name' is created here.


### Accessing Attributes Through an instance

The next step is to access an object's attributes which can be done using the dot operator '.' you might recognise it from earlier in the docstrings section.

```python
instance_name.data
instance_name.method()
 ```

Returning to Potato, we are now going to create an object tato which is a uni-tato (a cross of a unicorn and a potato).

```python
class Potato:
    "This class is a template of different types of potatoes"


    def info(self,kind):
       self.kind = kind


tato = Potato()
tato.info('uni-tato')
print('Type of potato is:',tato.kind)
```

Output:

```
Type of potato is: uni-tato
```

***
## [Wanna know more??](https://github.com/vhawk19/Py_Primer/blob/master/Classes/Class_Variables.md)

