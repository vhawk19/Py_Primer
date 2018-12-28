A simple file program  
new_file = open("test.txt", "w") 
new_file.write("Writing text to file. This is the first line.\n"+\ "And the second line.")
 new_file.close()

Let us try to understand each line of code in the above program
Open() function
On the first line, we use open function. The open() function takes two parameters; filename, and mode.
Filename: This is a string telling Python where to find the file. If you’re using Windows, you saved test.txt to the local disk on the D: drive, so you specify the location of your file as d:\\test.txt
Mode
There are four different methods (modes) for opening a file:
"r" - Read - Default value. Opens a file for reading, error if the file does not exist
"a" - Append - Opens a file for appending, creates the file if it does not exist
"w" - Write - Opens a file for writing, creates the file if it does not exist
"x" - Create - Creates the specified file, returns an error if the file exists
In addition you can specify if the file should be handled as binary or text mode
"t" - Text - Default value. Text mode
"b" - Binary - Binary mode (e.g. images)
Write()
In the second line, we have the write function. Inside the write function, we specify the content we want write into our file
Close()
Finally, we need to tell Python when we’re finished writing to the file, using the close function:
We have successfully created a new file and entered some contents to it. Now let us try to read the contents from a file. Let us continue with the above example
new_file = open("test.txt", "w") 
print(new_file.read()) 
new_file.close()

