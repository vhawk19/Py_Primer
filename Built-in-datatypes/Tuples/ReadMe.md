**Author:** Anagha Sivadas T

***

# Tuples

Tuples are immutable sequences, typically used to store collections of heterogeneous data

Tuples may be constructed in a number of ways:

 *  Using a pair of parentheses to denote the empty tuple: `()`
 *  Using a trailing comma for a singleton tuple: `a,` or `(a,)`
 *  Separating items with commas: `a, b, c` or `(a, b, c)`
 *  Using the `tuple()` built-in: `tuple()` or `tuple(iterable)`

 Examples
 1. Input: 
 ```python
 x=tuple('abc')  
 print(x)
 ``` 
   
   Output: `('a', 'b', 'c')` 
 
 2. Input: 
```python
 y=tuple( [1, 2, 3] )  
 print(y)
```
    
    
  Output: `(1, 2, 3)`
 
 3. Input: 
 ```python
              z=tuple()  
              print(z)
 ```
 Output: 
    `()`


**Note:** It is actually the comma which makes a tuple, not the parentheses. The parentheses are optional, except in the empty tuple case, or when they are needed to avoid syntactic ambiguity. 
