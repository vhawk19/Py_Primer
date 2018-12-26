<!--Lambda Expressions in Python-->
# Lambda Expressions

**_Lambda expressions_** allow us to create an anonymous function. We can quickly make functions for a particular purpose without having to properly define a function using `def`.

**_Lambda expressions_** are a single statement. They work exactly like functions created using `def`. The only key difference is that their result is typed in as an expression and doesnt need to be explicitely returned.

***

### Example:

_Imagine we have a function `square()` which returns the square of an argument passed to it,_
```python
def square(x):
    return x*x
square(5)

#Output : 25
```
_We can instead write this as a lambda expression as,_
```python
#We do not usually assign a lambda expression to a variable. This is just for demonstration purposes.
square = lambda x: x*x
square(5)

#Output : 25
```

***

**_Lambda expressions_** are usually used in combination with other functions like map and filter.

map()
---
`map()` function allows us to "map" a function to an iterable object. i.e. The functions is called and executed for each element of the iterable object. However inorder to get results from `map()` we need to eiither iterate through map or simply cast it to a list.

### Example:

```python
def square(x):
    return x**2
m=[1,2,3,4,5] #list
l=map(square,m)
print(l)

#Output : [1,4,9,16,25] 

#OR

def square(x):
    return x**2
m=[1,2,3,4,5] #list
print(list(map(square,m)))

#Output : [1,4,9,16,25]
```
_This can be written using lambda expressions as,_

```python
a=[1,2,3,4,5]
l=map(lambda x: x**2,a)
print(l)

#Output : [1,4,9,16,25]
```

filter()
---
It recieves a function and an iterable object as arguments. The function should return true or false value. U will get back only those elements as results which when passed through the function return True.

### Example:

```python
m=[1,2,3,4,5]
def check_even(x):
    return x%2==0 
even=filter(check_even,m)
print(even)

#Output : [2,4]

#OR

m=[1,2,3,4,5]
def check_even(x):
    return x%2==0 
print(list(filter(check_even,x)))

#Output : [2,4]
```
_This can be written using lambda expressions as,_
```python
m=[1,2,3,4,5]
print(list(filter(lambda x: x%2==0,m)))

#Output : [2,4]
```

***

## More Examples:

_1.Lambda expression to grab first character of a string_
```python
lambda s: s[0]
```

_2.Lambda expression to reverse a string_
```python
lambda s: s[::-1]
```

**NOTE:_LAMBDA EXPRESSIONS_ CAN ALSO TAKE MULTIPLE ARGUMENTS**

_3.Lambda exression to add two numbers_
```python
lambda x,y: x+y
```

***
***
    
    
    
