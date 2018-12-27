**Author:** Ashley T Roy

**Edits:** S Sandeep Pillai

***

# Lists

* Lists are a collection which is ordered and changeable.
* It can contain different data types. 
* Lists are written within square brackets.
* They also allow duplicate elements.

# List Declaration

## Empty list
An empty list is declared using square brackets.
```python
l=[]
```
## List with values
Values can be given to the list during declaration by separating the elements with commas.
```python
l=[12,23.2,"abc",12]
```
## List declaration using type constructor
```python
list(values)
```
## List declaration through iterations
```python
[x for x in iterable]
```
Example:
```python
a=[x for x in range(2)]
```
Here, `a=[0,1]`.

# Nested Lists
A list can even have another list as an element. This is called nested list.
```python
# nested list
my_list = ["mouse", [8, 4, 6], ['a']]
```
# List Indexing

All elements in the list are ordered from 0 to n-1 where n is the number of elements in the list.

In the above example:
```python
l[0]=12
l[1]=23.2
l[2]="abc"
l[3]=12
```

Trying to access an element other than 0 to 3 indices will raise an `IndexError` and not providing an integer value as index will create a `TypeError`.

## Negative Indexing
The index of -1 refers to the last item, -2 to the second last item and so on.

Example:
`l=[1,2,3,4,5]`.
Here, `l[-1]` is `5` and `l[-2]` is `4`.

## Indexing for nested lists
We use nested indexing in such cases.

Example: `l=[1,[2,3,4],6,[4,8,12]]`. Here, 

```python
l[0]=1
l[1]=[2,3,4]
l[1][0]=2
l[1][1]=3
l[1][2]=4
l[2]=6
l[3]=[4,8,12]
l[3][0]=4
l[3][1]=8
l[3][2]=12
```
# Slice Operator

Slice operation is used to access a specified range elements in a list.

General syntax:  `list_name[start:stop:step]`

* **Start** - starting integer where the slicing of the object starts.
* **Stop** - integer until which the slicing takes place. The slicing stops at index stop - 1.
* **Step** (optional) - integer value which determines the increment between each index for slicing. By default, this value is 1.

If no value is given for start and stop, it considers the beginning and the end of the list respectively.

Examples:

1. Input: `print(l[2:5])`

	Output: `[3,4,5]`

2. Input: `print(l[:3])`

	Output: `[1,2,3]`
3. Input: `print(l[2:])`

	Output: `[3,4,5]`
	
# Adding elements into an already existing list

## Append function
`append()` adds an element to end of the list.

Syntax: `list_name.append(value)`

Example: 
```python
l=[1,2,3]
n=[4,5]
l.append(n)
```
Now, `l=[1,2,3,[4,5]]`

This function adds only ***one element*** to the list at a time.

## Extend function
`extend()` adds multiple elements to the end of the list.

Syntax: `list_name.extend(values)`

Example:
```python
l=[1,2,3]
n=[4,5]
l.extend(n)
```
Now, `l=[1,2,3,4,5]`.

**Note:** Only one argument can be given for `extend()`.

## + Operator
`+` is used to concatenate 2 lists.

Example:
```python
l=[1,2]
n=[3,4,5]
x=l+n
```
Here, `x=[1,2,3,4,5]`

## Insert function

`insert()` is used to add an element at the given index.

Syntax: `list_name.insert(index,value)`

Example:
```python
l=[1,2,3]
l.insert(1,10)
```
Now, `l=[1,10,2,3]`.

# Deleting elements from a list

## Del function

Syntax: `del(list_name[index])`

Example: 
```python
l=[1,2,3,4]
del(l[2])
```
Now, `l=[1,2,4]`

Multiple elements can be deleted using `del()` by slicing.

Example:
```python
l=[1,2,3,4,5,6]
del(l[1:4])
```
Now, `l=[1,5,6]`.

## Remove function
`remove()` is used when index is unknown.

Syntax: `list_name.remove(value)`

Example:
```python
l=[1,2,3,4,3]
l.remove(3)
```
Now, `l=[1,2,4,3]` since only the first occurence of the element is considered.

## Pop function
`pop()` returns and removes last element of the list.

Syntax: `list_name.pop()`

Example:
```python
l=[1,2,3,4,5]
l.pop()
```
Here, `5` is returned and `l=[1,2,3,4]`.

Index can also be given in the parantheses to remove a specific element in the list.

# Other Functions

## Len function
`len()` returns the length of the list.

Example:
```python
l=[1,2,3,4]
print(len(l))
```
Output: `4`

## Reverse function
`reverse()` is used to reverse the order of elements in the list and this function does not return anything.

Syntax: `list_name.reverse()`

Example:
```python
l=[1,2,3,4]
l.reverse()
```
Now, `l=[4,3,2,1]`.

## Sort function
`sort()` is used to sort the elements in the list in ascending order or alphabetical order in case of integers and strings respectively.
This function will not work if integer/float and string values are present in the list to be sorted.

Syntax: `list_name.sort()`

Example:
```python
l=[8,12,36,29,4]
l.sort()
```
Now, `l=[4,8,12,29,36]`.

For sorting in descending order, we use the following syntax:
```python
list_name.sort(reverse=True)
```

**NOTE: The sort() function is NOT the same as the sorted() function. sort() is a subfunction of list datatype which `CANNOT` be used for other datatypes such as tuples or dictionaries.** 

`

## Max and min functions
`max()` and `min()` functions return the maximum and minimum values in the list respectively.

Syntax: `max(list_name)`

Example:
```python
l=[5,6,3,8,1,9]
print(max(l))
```
Output: `9`

## Count function
`count()` returns the number of occurences of the given value in the list.

Synatx: `list_name.count(value)`

Example:
```python
l=[1,4,2,8,4,1,8,9,8]
print(l.count(8))
```
Output: `3`

## Index function

`index()` returns the index of the given value.

Syntax: `list_name.index()`

Example:
```python
l=[1,2,3,4,5,6]
print(l.index(4))
```
Output: `3`

In case of multiple occurences of a value, the first occurence is considered.

***
