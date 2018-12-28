## Reading from a file
In the page you have learned how to write into a file. Now let us understand how to read from a file. 

Previously we have created a new file , located in the same folder as Python havong the following contents in it:
```
This is my first python program.I am really excited about it
```
To read a file in Python, we must open the file in reading mode.

The above program prints out the content of new_file
By default the read() method returns the whole text, but you can also specify how many character you want to return using read(size) method 
Example

 new_file = open("test.txt", "w") 
print(new_file.read(3)) 
new_file.close()

Read()
The above program prints out the content of new_file
By default the read() method returns the whole text, but you can also specify how many character you want to return using read(size) method 
Example

 new_file = open("test.txt", "w") 
print(new_file.read(3)) 
new_file.close()
