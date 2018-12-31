**Authors:** Annu Jolie

**Edits:** Pranav Shridhar, Diya Maria Deepak

***


## Reading the entire file in a go
In the previous page you have learned how to write into a file. Now let us understand how to read from a file. 

<img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Reading-297450.png"  width="250" height="250" float="left"/>

Previously we have created a new file, called "test.txt" having the following contents in it :
```
This is my first python program.
I am really excited about it!!
```
To read a file in Python, we must open the file in read mode.Then we use read() method for reading the content of the file :

```python
f = open("test.txt", "r")
print(f.read())
```
The above program prints out the content of test.txt file. Once the end of file is reached, we get empty string on further reading.

_____________________________________________________

## Reading only Parts of the File
By default the read() method returns the whole text, but you can also specify how many character you want to return using read(size) method. Here 'size' is the number of bytes to be read from the opened file.

**_Example_**
```python
new_file = open("test.txt", "r") 
print(new_file.read(13)) 
new_file.close()
```
The output of the code will be :-
```python
This is my fi
```
_____________________________________________________


### Read the file line by line
You can read the contents of a file, line by line by using the readline() method.If have a very long file, readline() method is more efficient and convenient

**_Example I_** - Read one line of the file :

```python
f = open("test.txt", "r")
print(f.readline())

```
The output of the code will be :-
```python
This is my first python program.
```

**_Example II_** - By calling readline() two times, you can read the two first lines :

```python
f = open("test.txt", "r")
print(f.readline())
print(f.readline())

```
The output of the code will be :-
```python
This is my first python program.
I am really excited about it!!
```

