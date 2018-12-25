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
