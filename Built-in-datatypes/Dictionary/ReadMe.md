:no_entry_sign: **WORK IN PROGRESS** :no_entry_sign:

# Dictionary
### What is a dictionary?:books:
Let's assume u wanna lookup the meaning of a particular word. What do you do? You open up your dictionary!! You try to figure where this word lies by having a vague idea about its lexicographic position and try to find it. Once you find the word "Hooray!!", now all you got to do is read the meaning written beside it.<br><br>
That's how conventional dictionaries work. You have a key, which is the word itself and a value which is the meaning of the word you were searching for. So basically you were using the word (key) as a way of finding the meaning (value). Hence we can say that the dictionary in real life is a huge collection of word-meaning pair (key-value pair), in which we are using the word as the means of accessing the meaning. Turns out that's more or less what dictionaries in python are too! It is a collection of key-value pairs in which keys are used to access the values.

### Let's create a dictionary in python

Now let's create our own dictionary, and let's keep a name for it. Just like Cambridge has one dictionary oxford another, We are going to create a new dictionary with the name my_dict. The syntax for doing the same is as follows:
```python
my_dict={}
```
What this piece of code does in python is create a new empty dictionary, with the name my_dict. Anytime we want to access something from the dictionary or write something from the dictionary we use the name of the dictionary first and then continue.<br>
Now I want to add word-meaning pairs to it. For that, all I have to do is:
```python
my_dict['truth']='the quality or state of being true.'
```
What we are doing here is we are defining the meaning for a word 'truth' and adding it to the dictionary. Since we use the word to access the meaning the information is also stored in a similar manner. The meaning of the word 'truth' can be accessed by the key truth from the dictionary my_dict. Hence the genral syntax follows:
```python
dict_name[key]=value
```
