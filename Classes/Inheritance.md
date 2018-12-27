**Author(s): Mohita Liza Bipin, Pranav Shridhar**

# Inheritance

A class can inherit attributes from an other class called a super or parent class,
the former is called the child class

Compare this to fruit.Apples and strawberries are both fruits and have
the same basic prequisites for a typical fruit but each their own characteristics
In this situation the parent class would be fruit and the child classes would be
the apple and strawberry classes

### Syntax

The syntax is fairly simple.

```python
class class_name (super_class_name):
    #body
   ```

### Time for an example

So lets see an example based on the earlier one of fruits

```python
class fruit():

    def print_fruit(self):
        print("Contains seeds\n")


class Apple(fruit):

    def print_apple(self):
        print("I'm an apple!")


class Strawberry(fruit):
    def print_strawberry(self):
        print("I'm a strawberry")

```

As before Strawberry and Apple inherit from fruit which means all of their
objects will have the attributes of the class fruit but why should you believe me?
Lets test it out by creating objects and seeing what happens

```python
a = Apple()
s = Strawberry()

a.print_apple()
a.print_fruit()

s.print_strawberry()
s.print_fruit()
```


Output:

```python
I'm an apple!
Contains seeds

I'm a strawberry
Contains seeds
```
As you can see from the output both objects can access the attributes of the parent class

***
## [How about inheriting some theory now??](https://github.com/vhawk19/Py_Primer/blob/master/Classes/theory.md)
