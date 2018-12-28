**Author:** S Sandeep Pillai

**Edit(s):** Pranav Shridhar

***

Now let us look at some of the inbuilt functions (that you need to byheart lol).

# Inbuilt Functions

Modules are basically header files in python, which you can `link` in your program to get access to a vast collection of 
functions and features. 

To 'import' a module into your program, you can use the following syntax:

```python

import modulename

```
That's it! Now you can use the vast amount of functions and features that the module provides in your program, without having
to write new functions yourself!

## Math Module

```python
import math
```

The math module contains various functions that can be useful for mathematical functionality in your program. A few useful
functions include:

### math.pow( a , b )  

`This function will output the number "a raised to the power b"`

```python
math.pow(2,3)     # Input
>>> 8             # Output
```
### math.sqrt(a) 

`This function will output the square root of a`

```python
math.sqrt(49)     # Input
>>> 7             # Output
```

### math.sin(a)

`This function will return the trignometric sine ratio of a *radians* `

```python
math.sin( math.pi / 2 )     # Input: math.pi can be used to get an accurate value of π
>>> 8                       # Output
```
### math.log10(a)

`This function will return the log a to the base 10 value.`

```python
math.log10(1000)         # Input
>>> 3                    # Output
```

By now, if you are tired of typing out 'math' repeatedly, you can opt for a shorthand style as follows :

```python
import math as m
m.sin(m.pi/2)         # Input
>>> 8                 # Output
```

Below I shall list a few more important functions that can be useful:

```python

abs(x-y) 
# Basically acts as a modulus function, giving the distance between x and y. Note that abs isnt part of the math module.

math.ceil(x) 
# Returns the smallest integer greater than x, i.e 1.2 will give 2 as the output. Think Ceiling - Above.

math.floor(x)
# Returns the smallest integer lesser than x, i.e 1.2 will give 1 as the output. Think Floor - Below.

math.exp(x)   
# Returns e^x  

```

# Composition of functions

Functions have a very useful feature where we can give a specific function as an argument for another function. This is 
particularly useful in the following example:

```python

math.pow( math.sin(π/6) , 2)  # Input: (sin30)^2
>>>0.25                       # Output
```

***


## [Wanna know about lambda functions and its fancy features??](https://github.com/vhawk19/Py_Primer/blob/master/Functions/3_Lambda_Expressions.md)
