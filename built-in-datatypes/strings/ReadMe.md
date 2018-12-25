# String

* Textual data in python is handled by str objects(strings)
* They are immutable sequences of Unicode code points.
They can be written in a variety of ways
```python
# Single quotes
'allows embedded double quotes like these "" '

# Double quotes
'allows embeded single quotes like these '' "

#triple Double/Single quote, these can span across multiple lines(all associated whitespce charecters will be included in the string) 
'''tripled single quote which allows for embedded double quotes'''
"""tripled double quotes which allows for embedded single quotes"""
String literals in python are surrounded by either single quotation marks, or double quotation marks.

```
* Strings maybe constructed from other objects using the **str** function
```python
a=str(10)
#here a is nothing but a string "10"/'10'
```

Strings can be output to screen using the print function. For example: print("hello").

Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string.

```
a="this is a string"
```

# Printing String Literals

String literals can be printed using the print function.

Use ' ' **single quotes** or " " **double quotes** for single line printing and ''' ''' **three single quotes** for multi line printing.
```
print('Hello World')
print("Hello World")
print('Hello\nWorld')
print('''Hello
         World''')
```
Output:
```
Hello World
Hello World
Hello
World
Hello
World
```

# String Methods

### str.capitalize()
Return a copy of the string with its first character capitalized and the rest lowercased.

```python
a="lorem ipsum dolor sit amet"
a.capitalize()
print(a)
#Output: Lorem ipsum dolor sit amet
```
### str.center(width[, fillchar])
Return centered in a string of length width. Padding is done using the specified fillchar (default is an ASCII space). The original string is returned if width is less than or equal to len(s).

```python
a="lorem ipsum dolor sit amet"
a.center(40," ")
#Output:'       lorem ipsum dolor sit amet       '
a.center(40,"*")
#Output:'*******lorem ipsum dolor sit amet*******'
```
### str.count(sub[,start[,end]])
Return the number of non-overlapping occurrences of substring sub in the range [start, end]. Optional arguments start and end are interpreted as in slice notation.

```python
a="lorem ipsum dolor sit amet"
a.count('i')
#Output:2
a.count('i',7)
#Output:1 
a.count('i',7,9)
#Output:0
```
### str.endswith(suffix[,start[,end]])
Return True if the string ends with the specified suffix, otherwise return False. suffix can also be a tuple of suffixes to look for. With optional start, test beginning at that position. With optional end, stop comparing at that position.

```python
a='lorem ipsum dolor sit amet"
a.endswith('amet')
#Output:True
a.endswith('dolor')
#Output:False
a.endswith('amet',1)
#Output: True
a.endswith(amet,1,2)
#Output:False
```
### str.find(sub[, start[, end]])

Return the lowest index in the string where substring sub is found within the slice s[start:end]. Optional arguments start and end are interpreted as in slice notation. Return -1 if sub is not found.

```python
a="lorem ipsum dolor sit amet"
a.find("ipsum")
#Output:6
a.find("ipsum",7)
#Output:-1
a.find("ipsum",7,10)
#Output:-1
```
