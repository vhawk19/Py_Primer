<!--Lambda Expressions in Python-->
_Author : Ashley Thomas Roy_
***
# Lambda Expressions :sweat_smile:

**_Lambda expressions_** allow us to create an anonymous function. We can quickly make functions for a particular purpose without having to properly define a function using `def`.

**_Lambda expressions_** are a single statement. They work exactly like functions created using `def`. The only key difference is that their result is typed in as an expression and doesn't need to be explicitly returned.

***

### Example:

_Imagine we have a function `square()` which returns the square of an argument passed to it,_
```python
def square(x):
    return x*x
square(5)

#Output: 25
```
_We can instead write this as a lambda expression as,_ :heavy_check_mark:
```python
#We do not usually assign a lambda expression to a variable. This is just for demonstration purposes.
square = lambda x: x*x
square(5)

#Output: 25
####Seeeeee! Much easier.....Still confused? More examples coming up!
```

***

**_Lambda expressions_** are usually used in combination with other functions like map and filter.

map()
---
`map()` function allows us to "map" a function to an iterable object, i.e., the function is called and executed for each element of the iterable object. However, in order to get results from `map()` we need to either iterate through the map or simply cast it to a list.

### Example:

```python
def square(x):
    return x**2
m=[1,2,3,4,5] #list
l=map(square,m)
print(l)

#Output: [1,4,9,16,25] 

#OR (No need to learn both....CHILL!!!)

def square(x):
    return x**2
m=[1,2,3,4,5] #list
print(list(map(square,m)))

#Output: [1,4,9,16,25]
```
_This can be written using lambda expressions as,_ :heavy_check_mark:

```python
a=[1,2,3,4,5]
l=map(lambda x: x**2,a)
print(l)

#Output: [1,4,9,16,25]
```

filter()
---
It receives a function and an iterable object as arguments. The function should return a true or false value. U will get back only those elements as results which when passed through the function return True.

### Example:

```python
m=[1,2,3,4,5]
def check_even(x):
    return x%2==0 
even=filter(check_even,m)
print(even)

#Output: [2,4]

#OR

m=[1,2,3,4,5]
def check_even(x):
    return x%2==0 
print(list(filter(check_even,x)))

#Output: [2,4]
```
_This can be written using lambda expressions as,_ :heavy_check_mark:
```python
m=[1,2,3,4,5]
print(list(filter(lambda x: x%2==0,m)))

#Output: [2,4]
```

***

## More Examples:

_1.Lambda expression to grab the first character of a string_
```python
lambda s: s[0]
```

_2.Lambda expression to reverse a string_
```python
lambda s: s[::-1]
```

**:eight_spoked_asterisk: :_LAMBDA EXPRESSIONS_ CAN ALSO TAKE MULTIPLE ARGUMENTS :scream_cat:**

_3.Lambda expression to add two numbers_
```python
lambda x,y: x+y
```

***                                                                                                                
***
That was EZ :sunglasses: 
    
    
