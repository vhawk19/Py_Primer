# Lists

* Lists are a collection which is ordered and changeable.
* It can contain different data types. 
* Lists are written within square brackets.
* They also allow duplicate elements.

# List Declaration

## Empty list
An empty list is declared using square brackets.
```
l=[]
```
## List with values
Values can be given to the list during declaration by separating the elements with commas.
```
l=[12,23.2,"abc",12]
```
## List declaration using type constructor
```
list(values)
```
## List declaration through iterations
```
[x for x in iterable]
```
Example:
```
a=[x for x in range(2)]
```
Here, ```a=[0,1]```.

# Nested Lists
A list can even have another list as an element. This is called nested list.
```
# nested list
my_list = ["mouse", [8, 4, 6], ['a']]
```
# List Indexing

All elements in the list are ordered from 0 to n-1 where n is the number of elements in the list.

In the above example:
```
l[0]=12
l[1]=23.2
l[2]="abc"
l[3]=12
```

Trying to access an element other than 0 to 3 indices will raise an ```IndexError``` and not providing an integer value as index will create a ```TypeError```.

## Negative Indexing
The index of -1 refers to the last item, -2 to the second last item and so on.

Example:
```l=[1,2,3,4,5]```.
Here, ```l[-1]``` is ```5``` and ```l[-2]``` is ```4```.

## Indexing for nested lists
We use nested indexing in such cases.

Example: ```l=[1,[2,3,4],6,[4,8,12]]```. Here, 

```l[0]=1```

```l[1]=[2,3,4]```

```l[1][0]=2```

```l[1][1]=3```

```l[1][2]=4```

```l[2]=6```

```l[3]=[4,8,12]```

```l[3][0]=4```

```l[3][1]=8```

```l[3][2]=12```
