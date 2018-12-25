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
a.endswith('amet',1,2)
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
### str.format(\*args,\*\*kwargs)
Perform a string formatting operation. The string on which this method is called can contain literal text or replacement fields delimited by braces {}. Each replacement field contains either the numeric index of a positional argument, or the name of a keyword argument. Returns a copy of the string where each replacement field is replaced with the string value of the corresponding argument.
```python
a="lorem ipsum dolor sit amet is {0}"
a.format(1+2)
#Output:'lorem ipsum dolor sit amet is 3'
```
### str.isalpha()
Return true if all characters in the string are alphabetic and there is at least one character, false otherwise. Alphabetic characters are those characters defined in the Unicode character database as “Letter”, i.e., those with general category property being one of “Lm”, “Lt”, “Lu”, “Ll”, or “Lo”. Note that this is different from the “Alphabetic” property defined in the Unicode Standard.
```python
a="lorem ipsum dolor sit amet"
a.isalpha()
#Outpu:True
```
### str.isalnum()
Return true if all characters in the string are alphanumeric and there is at least one character, false otherwise. A character c is alphanumeric if one of the following returns True: c.isalpha(), c.isdecimal(), c.isdigit(), or c.isnumeric().
```python
a="lorem ipsum dolor sit amet"
a.isalnum()
#Output:True
```
### str.isdecimal()
Return true if all characters in the string are decimal characters and there is at least one character, false otherwise. Decimal characters are those that can be used to form numbers in base 10, e.g. U+0660, ARABIC-INDIC DIGIT ZERO. Formally a decimal character is a character in the Unicode General Category “Nd”.

```python
a="lorem ipsum dolor sit amet"
a.isdecimal()
#Output:False
```
### str.isdigit()
Return true if all characters in the string are digits and there is at least one character, false otherwise. Digits include decimal characters and digits that need special handling, such as the compatibility superscript digits. This covers digits which cannot be used to form numbers in base 10, like the Kharosthi numbers. Formally, a digit is a character that has the property value Numeric_Type=Digit or Numeric_Type=Decimal.

```python
a="lorem ipsum dolor sit amet"
a.isdigit()
#Output:False
```

### str.islower()
Return true if all cased characters [4] in the string are lowercase and there is at least one cased character, false otherwise.

```python
a="lorem ipsum dolor sit amet"
a.islower()
#Output:True
```
### str.isspace()
Return true if there are only whitespace characters in the string and there is at least one character, false otherwise. Whitespace characters are those characters defined in the Unicode character database as “Other” or “Separator” and those with bidirectional property being one of “WS”, “B”, or “S”.

```python
a="lorem ipsum dolor sit amet"
a.isspace()
#Output:False
```
### str.istitle()
Return true if the string is a titlecased string and there is at least one character, for example uppercase characters may only follow uncased characters and lowercase characters only cased ones. Return false otherwise.
```python
a="lorem ipsum dolor sit amet"
a.isspace()
#Output:False
```
### str.isupper()
Return true if all cased characters [4] in the string are uppercase and there is at least one cased character, false otherwise.
```python
a="lorem ipsum dolor sit amet"
a.isupper()
#Output:False
```

### str.join(iterable)
Return a string which is the concatenation of the strings in iterable. A TypeError will be raised if there are any non-string values in iterable, including bytes objects. The separator between elements is the string providing this method.

```python
a="lorem ipsum"
b=['1','2','3','4']
a.join(b)
#Output:'1lorem ipsum2lorem ipsum3lorem ipsum4'
```
