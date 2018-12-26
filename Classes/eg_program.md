```python
class Car:
    def __init__(self, capacity, type, color, model): # Initiates instance/object

        # Attributes (Instance variables, in this case, since it is declared inside '__init__ method')
        self.capacity = capacity
        self.type = type
        self.color = color
        self.model = model


    # Methods
    def __repr__(self):  # Reproduces object as output in a user friendly manner. Fallback to '__str__'
        return f"Car({self.capacity},{self.type},{self.color},{self.model})"

    def __str__(self):  # Outputs a string as output for an object.
        return (f'{self.capacity},{self.type},{self.color},{self.model}')

    def oldOrNew(self):  # Regular method -> requires instance(object) variable 'self'
        if 2018-self.model >= 2:
            return 'Old car'
        else:
            return 'New car'

    @classmethod  # Decorator -> used for altering the behaviour of a function
    def someFunc(cls):  # Class method -> requires class variable 'cls'
        pass

    @staticmethod
    def anotherFunc():  # Static method -> does not require either class or instance variable. Independent function
        pass


class Chevrolet(Car):
    def __init__(self, capacity, type, color, model):
        super().__init__(capacity, type, color, model) # Inherits instance(object) variables from super class (Car)
        # Car.__init__(self, capacity, type, color, model) #same output -> useful for multilevel and other higher forms of inheritance where class name is specific.


class Camaro(Chevrolet): # Multilevel Inheritance (Camaro inherits from Chevrolet which in turn inherits from Car)
    pass

# Objects' creation
car1 = Car(2, 'SUV', 'blue', 2010)
car2 = Car(1.5, 'Sedan', 'black', 2017)
chev1 = Chevrolet(3, 'MUV', 'red', 2012)
camaro1 = Camaro(4, 'sports', 'yellow', 2015)

# Accessing attributes and methods using 'dot' operator
car1.oldOrNew()
print(car1)
chev1.oldOrNew()
print(chev1)
print(camaro1.oldOrNew())
help(camaro1)
```
