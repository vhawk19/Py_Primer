**Author(s): Mohita Liza Bipin**

**Editor(s): Pranav Shridhar** 


# Class Variables

### Declaration

A class variable or static variable is shared by all objects of a class.

Let's use the example of a bookshop whose items are objects of class 'Items'.

```python
class Items:
    type = "book"
    def enter_info(self, name, genre):
        self.name = name
        self.genre = genre

    def print_info(self):
        print("Title : ", self.name, "\nGenre : ", self.genre, "\n\n")
```

The data member ```type``` is the same for each object as every item in the
book store is the same (and is a book).

Looking further into the topic let's create a few objects and call the methods
for both and see what happens.

```python

Book1= Items()
Book2= Items()
Book1.enter_info("The Hitchhiker's Guide to the Galaxy", "Comic Science Fiction")
Book2.enter_info("The Stanger", "Philosophical Fiction")

Book1.print_info()
Book2.print_info()
```

The output will be : 

```
Title: The Hitchhiker's Guide to the Galaxy
Genre: Comic Science Fiction
Type: book


Title: The Stanger
Genre: Philosophical Fiction
Type: book
```

Notice how the type for both is the same? Well, that's how a class variable
is. It's the same for all instances of the class.

### Altering a Class Variable

The correct way to alter a class variable is by accessing the static variable
through the **class name** and **not object name**

``` class_name.class_variable_name```

So let's try it out using 'Items' again :

```python

Book1= Items()
Book2= Items()

Items.type="I am an awesome book!" #IMP

Book1.enter_info("The Hitchhiker's Guide to the Galaxy", "Comic Science Fiction")
Book2.enter_info("The Stanger", "Philosophical Fiction")

Book1.print_info()
Book2.print_info()
```

New output:

```
Title: The Hitchhiker's Guide to the Galaxy
Genre: Comic Science Fiction
Type: I am an awesome book!


Title: The Stanger
Genre: Philosophical Fiction
Type: I am an awesome book!
```

See how the value of the data member changed for both objects and not just
one? This shows that class variables are common to all objects of a class.

***
## [Alright...let's go ahead, Shall we?](https://github.com/vhawk19/Py_Primer/blob/master/Classes/Inheritance.md)
