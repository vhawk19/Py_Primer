##A simple file program  
_______________
Now let us try to write a simple python program to add text into an empty file
```python
new_file = open("test.txt", "w") 
new_file.write("Writing text to file. This is the first line.\n And the second line.")
new_file.close()
```


Seems overwhelming!!
Let us try to break it down andunderstand each line of code in the above program
```diff
+ Open() function

```

_____________________
On the first line, we have the open function.We declared the variable new_line to open a file named text.txt The open() function takes two parameters; filename and mode.

1. **Filename**: This is a string telling Python where to find the file. If you’re using Windows, you saved test.txt to the local disk on the D: drive, so you specify the location of your file as d:\\test.txt

2. **Mode**: Here we used "w" letter in our argument, which indicates write mode.This arguemen ttells python whether we are readinf from a file or writing into it. 
There are four different methods (modes) for opening a file:
"r" - Read - Default value. Opens a file for reading, error if the file does not exist
"a" - Append - Opens a file for appending, creates the file if it does not exist
"w" - Write - Opens a file for writing, creates the file if it does not exist
"x" - Create - Creates the specified file, returns an error if the file exists
In addition you can specify if the file should be handled as binary or text mode
"t" - Text - Default value. Text mode
"b" - Binary - Binary mode (e.g. images)


```diff
 * **write() function**

```
______________________________
In the second line, we have the write function. Inside the write function, we specify the content we want write into our file


```diff
+ * **close() function**

```
______________________________
Close()
Finally, we need to tell Python when we’re finished writing to the file, using the close function:
We have successfully created a new file and entered some contents to it. Now let us try to read the contents from a file. Let us continue with the above example

