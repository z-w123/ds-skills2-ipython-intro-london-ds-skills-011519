
# Ipython Notebook and Running Cells

**Welcome to programming!**
Ipython/Juptyer notebooks will be our primary tool when conducting data science. The first thing to know with this is that each cell block [of code] can be run be pressing **shift+enter**. Try running the (and tinkering) the below code blocks to see what returns:


```python
print('This is code being run.')
```

    This is code being run.


The Python language can also work as a calculator. Try running and editing the below cells and see what it returns


```python
2 + 2
```




    10




```python
(2/4) +(3 * 4)
# spaces don't matter
```




    12.5




```python
5 + 11
44 - 8 # notice that only the last line of code returns as the output
```




    36




```python
print(5 + 11)
44 - 8
# notice that the printed statement and the last line returns
```

    16





    36



# Jupyter Notebook Cell Types

You might have started to notice that the code blocks have little notes that say **In [ ]:** before you run them, and then are filled with a number after you run them. This is important, as it tells you what order cell blocks were run. (Which can sometimes affect how your code runs.)

You may also notice that other cell blocks, such as this one, do not have the **In [ ]:** label as with the code blocks. This is because this cell block is formatted as **Markdown** rather then code. You can see (and change) what type of cell is by clicking the dropdown menu at the top:
<img src="Jupyter_Notebook_Cell_Type_Dropdown.png" width=600>

## Markdown Format
Markdown can accept different formatting methods to display text and images in helpful ways. Doubleclick any Markdown cell in this notebook to see how it is written. Some quick tips:
* Headers are created by a # before the text. The more ##, the smaller the header
* Bullets are created with a *
* **Bold** words are surrounding the text with **
* *Italics* are made by surrounding the text with *
* Text can also be formatted as `code` by surounding the text with the backtick symbol, `

You can create ordered lists as well with numbers instead of *.
1. First point
2. Second point



You can create a table with | and -- between rows and columns like this:

| Col1 | Col2   |
|------|------|
|   1a  | 2a|
|   1b  | 2b|

You can also embed links in text in this format: `[link text](http://url)`

Here is a [helpful link](https://medium.com/ibm-data-science-experience/markdown-for-jupyter-notebooks-cheatsheet-386c05aeebed) for other Markdown formatting techniques:

https://medium.com/ibm-data-science-experience/markdown-for-jupyter-notebooks-cheatsheet-386c05aeebed

# Creating New Cells and Deleting Old Cells

As you expand your notebook, you can use common shortcut to create a new cell (instead of clicking the + symbol in the top left) either above or below the current cell you have selected.:
* Esc + a will create a new cell immediately above
* Esc + b will create a new cell immediately below
* Double tapping d will delete the currently selected cell

# Command Versus Edit Mode

You should also start to notice that when you are in a cell writing code (or notes), the cell is highlighted in **green** meaning you are in **edit mode**. 

Alternatively, if you **press esc**, the cursor will be in **blue** inidicating that you are in **command mode**.

### Edit Mode
Edit mode is the standard mode for editing cells, whether its writing code or notes.
To enter edit mode from command mode simply hit enter, or double click on a cell.

### Command Mode
In command mode, you can delete cells, add cells, copy cells, paste cells, change cell types, and more. You can also do these tasks in a more cumbersome (and time consuming) manner by using the various headers in the menu bar at top.
<img src="Jupyter_Menu.png" width=600>
You can also see a full list of shortcuts available in command and edit mode under the help menu.

<img src="Jupyter_Help_Menu.png" width=600>

# Running Bash Commands

We can also run bash commands just as we did before from the terminal directly within iPython notebooks!  
 (Note: bash commands cannot be mixed with python and must be in their own cell block.)   
 
Try it out!


```python
pwd
```


```python
ls
```

# Python Comments
You can write in plain english in a code cell but not have that line be run.


```python
# This is a comment. This line will not run
4+7 
# The line above will run because it is not 'commented out'
```




    11




```python
9 - 4 # everything after the # will be commented out, but the calculation will still run
```




    5



Note the green text following the **#** in the cell above. 

Anything following a **#** in python is a comment and will not execute. This is a useful feature for annotating your code with notes for yourself and other later so that your code is easy to read.

A shortcut to comment out code is, while your cursor is in the line you want to comment out, hit `Ctrl + /` and it will add a # at the front of the line

# Objects

In Python, we can define a **object** that is stored in memory. We can use that object, which represents whatever we want, in other lines of code. An object is also called a variable.

To define a variable or an object, simply use the equal sign:  

`variable_name = what_to_store_in_the_variable`

Always have the name of the object on the left side of the equals sign. Run and tinker the cells below with different or new objects.


```python
# let's make some objects!
a = 5
b = 9
```


```python
a + b
```




    14




```python
print(a * b)
```

    45



```python
word = 'apple'
word2 = 'pear'
print(word, word2)
```

    apple pear


# Object/Variable Types
You can also check what type of object something is using the built in **type()** method. This can be useful when determining how to work with an object that you are unfamiliar with. Basic object types are:
* int - Integer. This is a whole number
* str - String. This is a list of characters (aka text). 
* float - Float. This is a non-whole number (aka a number with decimal points)


```python
type(a)
```




    int




```python
type(word)
```




    str




```python
pi = 3.141
type(pi)
```




    float




```python
type(3.141)
```




    float



# Built in Python Functions

We have used one built in python functions: 
    * print() #Prints stuff!
In general, **python has reserved keywords** for built in functions like this. 
**Be sure to not name your variables any of these!**

<img src="python_built_in_functions.png" width=600>


```python
# let's try some of the built in functions!
len(word)
# returns the length of characters in a string object
```




    5




```python
list(word)
# turns a string object into a list of each character
```




    ['a', 'p', 'p', 'l', 'e']




```python
list(range(0, 10))
# returns a list of numbers between 0 (inclusive) and 10 (exclusive)
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]



# Handling Errors

Sometimes, the code cell you have written will not run. That is because it is not written in a way the Python language requires it. See what happens when you run the code below


```python
'apple' + 2
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-8-58195d5e30ca> in <module>()
    ----> 1 'apple' + 2
    

    TypeError: can only concatenate str (not "int") to str



```python
object_name
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-43-84d944bb2bcf> in <module>()
    ----> 1 object_name
    

    NameError: name 'object_name' is not defined


This is good for us! Reading and understanding errors will help you be a better coder. Always look to the last line to see the type of error we have to deal with. Then look up to see where the `---->` arrow points to. This will point to the line of problematic code that should be revised.
