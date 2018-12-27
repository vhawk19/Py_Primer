**Author:** [vhawk19](www.github.com/vhawk19)</br>
**Editor(s):**[Emmanuel Antony](https://github.com/emmanuelantony2000)


# String

* Textual data in python is handled by str objects(strings)
* They are immutable sequences of Unicode code points.
They can be written in a variety of ways
```python
# Single quotes
'allows embedded double quotes like these "" '
'Bob asked me,"Do you belive in unicorns?"'

# Double quotes
"allows embeded single quotes like these '' "
"I'm going fishing someday!"

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

```python
a="this is a string"
```

## Printing String Literals

String literals can be printed using the print function.

Use ' ' **single quotes** or " " **double quotes** for single line printing and ''' ''' **three single quotes** for multi line printing.
```python
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

## String Methods

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
Return True if the string ends with the specified suffix, otherwise return False. Suffix can also be a tuple of suffixes to look for. With optional start, test beginning at that position. With optional end, stop comparing at that position.

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
#Output:True
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
### str.ljust(width[, fillchar])
Return the string left justified in a string of length width. Padding is done using the specified fillchar (default is an ASCII space). The original string is returned if width is less than or equal to len(s).

```python 
a="lorem ipsum"
a.ljust(40,'*')
#Output:'lorem ipsum*****************************'
```

### str.lower()
Return a copy of the string with all the cased characters converted to lowercase
```python
a="LOREM IPSUM"
a.lower()
#Output:'lorem ipsum'
```
### str.lstrip([chars])
Return a copy of the string with leading characters removed. The chars argument is a string specifying the set of characters to be removed. If omitted or None, the chars argument defaults to removing whitespace. The chars argument is not a prefix; rather, all combinations of its values are stripped:

```python
a=' lorem ipsum' 
a.lstrip()
#Output:lorem ipsum 
a='lorem ipsum'
a.lstrip('lo')
#Output:rem ipsum
a='abababcfghasab'
a.lstrip('ab')
#Output:cfghasab All patterns of the given substring till another pattern is found will be stripped away starting form the left
```

### str.partition(sep)
Split the string at the first occurrence of sep, and return a 3-tuple containing the part before the separator, the separator itself, and the part after the separator. If the separator is not found, return a 3-tuple containing the string itself, followed by two empty strings.
```python
a='lorem ipsum'
a.partition(' ')
#Output:('lorem', ' ', 'ipsum')
```
### str.replace(old,new[,count])
Return a copy of the string with all occurrences of substring old replaced by new. If the optional argument count is given, only the first count occurrences are replaced.

```python
a='lorem ipsum'
a.replace('l','u')
#Output:'urem ipsum'
```

### str.rjust(width[ ,fillchar])
Return the string right justified in a string of length width. Padding is done using the specified fillchar (default is an ASCII space). The original string is returned if width is less than or equal to len(s).

```python
a='lorem ipsum'
a.rjust(40,'*')
#Output:'*****************************lorem ipsum'
```
### str.split(sep=None,maxsplit=-1)
Return a list of the words in the string, using sep as the delimiter string. If maxsplit is given, at most maxsplit splits are done (thus, the list will have at most maxsplit+1 elements). If maxsplit is not specified or -1, then there is no limit on the number of splits (all possible splits are made).

```python
a='lorem ipsum'
a.split()
#Output:['lorem', 'ipsum']
```

### str.splitlines([keepends])
Return a list of the lines in the string, breaking at line boundaries. Line breaks are not included in the resulting list unless keepends is given and true.

```python
a='''lorem
     ipsum'''
a.splitlines()
#Output:['lorem', 'ipsum']
```
### str.startswith(prefix[, start[, end]])
Return True if string starts with the prefix, otherwise return False. prefix can also be a tuple of prefixes to look for. With optional start, test string beginning at that position. With optional end, stop comparing string at that position.

```python
a='lorem ipsum'
a.startswith('lorem')
#Output:True
```
### str.title()
Return a titlecased version of the string where words start with an uppercase character and the remaining characters are lowercase.
```python
a='lorem ipsum'
a.title()
#Output:'Lorem Ipsum'
```
### str.upper()
return a copy of the string with all the cased characters converted to uppercase.

```python 
a='lorem ipsum'
a.upper()
#Output:'LOREM IPSUM'
```

