**Authors:** Annu Jolie

**Edits:** Pranav Shridhar, Diya Maria Deepak

***


## A simple file program  

Now let us try to write a simple python program to add text into an empty file.
<img src="http://eras4solutions.com/wp-content/uploads/2018/03/612948-BOS0148.gif"  width="150" height="150" />
```python
new_file = open("test.txt", "w") 
new_file.write("This is my first python program \n I am really excited about it!!)
new_file.close()
```

Let us try to break it down and understand each line of code in the above program.
### Line 1-
```diff
+  Open() function

```

On the first line, we have the open function.We declared a variable *new_line* to open a file named text.txt The open() function takes two parameters:- filename and mode.

1. **Filename**: This is a string tells Python where to find the file. If you’re using Windows, you saved test.txt to the local disk on the C: drive, so you specify the location of your file as c:\\test.txt

2. **Mode**: Here we used "w" letter in our argument, which indicates write mode.This arguement tells python whether we are reading from a file or writing into it. Other than "w", we have different other modes for opening a file

*Different methods (modes) for opening a file :*

* "r" - Read : Default value. Opens a file for reading, error if the file does not exist.
* "a" - Append : Opens a file for appending, creates the file if it does not exist.
* "w" - Write : Opens a file for writing, creates the file if it does not exist.

In addition you can specify if the file should be handled as binary or text mode
* "t" - Text : Default value. Text mode
* "b" - Binary : Binary mode (e.g. images)
_____________________
### Line 2-
```diff
+ write() function

```

Now we have successfully opened the file in write mode.In the second line, we have the write function. Inside the write function, we specify the content we want write into our file.

**Append() function**:-

If the file already exists, opening it in write mode clears out the old data and starts fresh, so be careful!!
Inorder to avoid this, we have the append function. The append function is used to append to the file instead of overwriting it.
To append to an existing file, simply open the file in append mode ("a"):
______________________________
### Line 3-
```diff
+ close() function

```

After writing into the file finally, we need to tell Python when we’re finished, by using the close function.It free up any system
resources taken up by the open file.Python automatically closes a file when the reference object of a file is reassigned to another file. However it is a good practice to use the close() method to close a file.

______________________________
   
   
We have successfully created a new file and entered some contents to it. Let us see one more example :-
     
   #### *Example II*


Here we open a file called *new.txt*. We have a *for loop* that runs over a range of 5 numbers.We use the write function to enter data into the file. 
```python
f= open("new.txt","a")
for i in range(5):
     f.write("This is line "+str((i+1))+"\n")
f.close()     
     
```
The result after code execution is as follows :-
```python
This is line 1
This is line 2
This is line 3
This is line 4
This is line 5     
```


Now let us try to read the contents from a file.
[                          Click here <img src="https://media.giphy.com/media/11tzAbXuJ0O4h2/giphy.gif"  width="35" height="35" />](https://github.com/annu12340/Py_Primer/blob/master/Learn%20to%20handle%20your%20file/Reading%20from%20a%20file.md)

