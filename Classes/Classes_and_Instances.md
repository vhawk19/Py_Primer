**Author(s):  Mohita Liza Bipin, Pranav Shridhar**

**Editor(s):**

# Classes and Instances
A class defines a set of attributes for an object and an object is an instance of a class.

Attributes include data members and methods.

Methods are essentially functions defined within a class and data members are variables which are also defined within a class

Yes, this seems a little complicated but it really isn't. Here's a simple analagy to help understand better:

A class is very similar to a basic recipe for a chocolate cake. It has all the ingredients (data) and the instructions (methods) to bake a cake.The object is the cake.

Many objects can be made from a class and these objects can also be called instances.
This process is called instantiation.

Now that the definitions are out of the way we'll be taking a closer look at class and instances.

## Classes

### Defining a Class

To define a class use the class key word followed by the class name.

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
    "This is a docstring syntax"
```


Now lets try applying this to our previous example, Potato.
```python
class Potato:
    "This class is a template of different types of potatoes"
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
    "This class is a template of different types of potatoes"


    def info(self,type):
       self.type= type
```

info is an example of a method and type is a data member.

'self' is a parameter as whenever a method is called the instance as a whole is passed automatically as the first parameter.


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


    def info(self,type):
       self.type= type


tato= Potato()
tato.info('uni-tato')
print('Type of potato is:',tato.type)
```

Output:
```
Type of potato is: uni-tato
```


