**Author:** S Sandeep Pillai
**Edited by:**


#Functions

**A function (or method) is defined as an named encapsulation of a specific set of instructions in a program.** 

In normal english, it can be considered as a package of lines of code that will be executed each time you 'call' it later on
in your program.

Now before we get into the boring theory, let us dwelve into how we can use functions in Python.

# Syntax

There are two kinds of functions within python: 
1) Implicit Functions
2) Explicit Functions

Implicit Functions are predefined functions within Python, or a module linked through Python. We shall focus on Explicit Functions 
for now.

## Stop it with the Theory! 

Okay, fine, so a function needs to be defined beforehand for it to be used later in the program. To define a function, we need
to use the following keywords:

''' 
'def' ''function-name'' ( 'Argument-1', 'Argument-2', ... 'Argument-N' )
    
    Line 1
    Line 2
        Line 2.1
        Line 2.2
        Line 2.3
    Line 3
    Line 4

#End of function-name
'''
Here, we use the keyword *'def'* to invoke the function definition clause so that the interpreter will know the following line
contains the definition of a function. To use this function later, simply follow the syntax:

'''

function-name( Arg1, Arg2, ArgN )  #This will execute Lines 1 to 4 once.

'''


##Advantages of using a function:

  * It allows for a significantly shorter length for the program code. 
  * You can reuse the code repeatedly instead of rewriting the same set of instructions again
