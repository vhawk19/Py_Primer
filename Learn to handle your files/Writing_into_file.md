## A simple file program  

Now let us try to write a simple python program to add text into an empty file
```python
new_file = open("test.txt", "w") 
new_file.write("This is my first python file program")
new_file.close()
```

Let us try to break it down and understand each line of code in the above program
## Line 1-
```diff
+  Open() function

```
_____________________
On the first line, we have the open function.We declared the variable *new_line* to open a file named text.txt The open() function takes two parameters:- filename and mode.

1. **Filename**: This is a string telling Python where to find the file. If you’re using Windows, you saved test.txt to the local disk on the D: drive, so you specify the location of your file as d:\\test.txt

2. **Mode**: Here we used "w" letter in our argument, which indicates write mode.This arguement tells python whether we are reading from a file or writing into it. Other than "w", we have different other modes for opening a file

*Different methods (modes) for opening a file:*

* "r" - Read - Default value. Opens a file for reading, error if the file does not exist
* "a" - Append - Opens a file for appending, creates the file if it does not exist
* "w" - Write - Opens a file for writing, creates the file if it does not exist

In addition you can specify if the file should be handled as binary or text mode
* "t" - Text - Default value. Text mode
* "b" - Binary - Binary mode (e.g. images)

## Line 2-
```diff
+ write() function

```
______________________________
Now we have successfully opened the file in write mode.In the second line, we have the write function. Inside the write function, we specify the content we want write into our file.
**Append() function**
When we use write function, it overwrites the file and the existing data in the file is lost.The append function is used to append to the file instead of overwriting it.
To append to an existing file, simply open the file in append mode ("a"):

## Line 3-
```diff
+ close() function

```
______________________________

After writing into the file finally, we need to tell Python when we’re finished, by using the close function.It free up any system
resources taken up by the open file.Python automatically closes a file when the reference object of a file is reassigned to another file. It is a good practice to use the close() method to close a file.

*********************************************************************************************************************************

We have successfully created a new file and entered some contents to it. Let us see one more example:-
```python
f= open("new.txt","a")
for i in range(5):
     f.write("This is line \n" ,(i+1))
f.close()     
     
```
Here we open a file called new.We have a for loop that runs over a range of 10 numbers.Using the write function to enter data into the file. The result after code execution is as follows:-
```python
This is line 1
This is line 2
This is line 3
This is line 4
This is line 5     
```


Now let us try to read the contents from a file.

