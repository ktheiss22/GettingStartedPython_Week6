# Getting Started with Python

## Basic Python Data Types

- Numbers
    - Note that, unlike bash, Python can handle _both_ integers and floating point (decimal) numbers.
    - Integers - `myInt = 10`
    - Floating point numbers (decimals) - `myFloat = 3.21312`
    - If running Python interactively, variable values can be seen just by typing the name of the variable - `myFloat`.
    - If running Python in a script, variable values can be printed by using the `print()` funtion - `print(myFloat)`.
    - Define myInt and myFloat as above. Now calculate `myInt / myFloat`. What type of number is the result? #Floating point number
    - Now try `float(myInt)` and `int(myFloat)`. What are the results? Look back at the values of `myInt` and `myFloat`. Have they changed?
    - Changing numbers from one type to another is one form of "type casting".
```
# Notes 2/22/22
- Jupyter notebook can mix python and markdown. 
- we can use this to create graphs stuff too
- helps keep projects organized 
- we can run juputer locallly with anaconda 
- dir -> directory. gives a list of the methods associated with that particular variable. 
    - methods with 2 underscores around the method are written this way because we do not want to execute them manually. but you can. 
- you have to allocate as much time you need when you use jupyter to access the notebook. it'll kick you off after time's up. 

- python is a dynaimcally typed language, it tries to automatically interpret the value we are providing (integer/floating)
- integer: whole numbers 
- floating point number: anything with a decimal
- in a script, we have to print the variable when using python. interctaively we can just type the variable name
- anything inside parenthesis is an argument 
- the word before the parenthesis is the function (verb of programing language) -> function(argument)
- myInt/myFloat (dividing myInt variable by the myFloat value) answer is floating point number
- float(myInt) -> take a data type and convert into what we need
- ("this is interpreted as a character, even if using numeric values") -> with quotation marks
- (integer value, no quotations. Will return numeric value) -> no quotation marks and cuts off the decimals. 
- formal term for what we are doing is called: type casting. 
- we often use strings, which is a series of individual characters. 
- individual letters, numbers, spaces are individual characters. 
- notebook in is an input out is an output on the left hand column. the numbers keep track of the order of commands we execute. 
```

- Strings - `myStr = "This is a string."`
    - Strings can be of any length, but are always defined with quotes.
    - Individual characters, or subsets of characters, can be accessed using square brackets - []
      - String indices (and all indices in Python) start at 0
      - `myStr = "biology"`
      - `myStr[0]`
      - A range of indices can be defined with a colon
      - `myStr[2:5]`
    - Strings can be concatenated together with the `+` operator.
      - `myStr = "biology"`
      - `newString = myStr + "_is_super_interesting"`
      - `newString`
```
Notes: 2/22/22
- myStr[0] -> extracts the first character of the string at index 0. 
- python starts counting from 0 not 1. 
- [] is called indexing, looking up an individual character. only use when a string has been created. 
- myStr[2:5] -> two numbers separated by a colon, this says 2,3,4,5 and counts the whole range of numbers. when we run this (4 characters) we get 3 characters returned 'is ' the space is a character. we do not get 4 because is exclusive of the last index and inclusive of the first 3 index. we need to go one more than what we want included. 
- myStr[-1] is counting in reverse -> we can only have 1 zero. -1 is the first character at the end. 0 is the first index counting forward. 
- we can glue strings together too, we can mix variables and literal and mix them too. 
- + is an example of an operator, and they do diffrerent things based on the type of variables we have. 
```
- Booleans - `True` or `False`
    - These variables can take the values `True` or `False` only.
      - `myBool = True`
    - These are the data types used in things like `if...else` statements and `while` loops.
    - Logical statements, like `myNum > 3` or `myStr == "test"`, return a boolean variable indicating the result of the comparison
    - In Python, the value of a Boolean can be reversed by preceding it with `not`.
```
# Notes 2/22/22
- takes only 2 values and they have to be exactly true or false. always has to be typed True with the T capitalized. or False. 
- we can do if else statements in python too. will print out if true or false and will not if the opposite. 
- booleans are the simplest possible variable. 
- we indent using tab or spacing, do not switch up between the two though. (3 spaces). 
- to test an if statement == (testing equality (==) that works with number or strings) 
- using 'is' is also a way to do testing equality. 
- using the testing equality != means not equal to 
```

## Functions

- Functions are the verbs of a programming language
- Functions take some variables or objects as input (arguments) and either do something with them or return a new variable/object.
- Functions are always written like this - `myFunction(object1,object2,...)`
- They _always_ have parentheses, even if they don't need any arguments to be passed to them
    - For example, `myFunction()`
- The number and type of arguments needed is specific to each function
- Perhaps the simplest function to use is `print()`. `print()` can take an arbitrary number of variables as arguments and will print them to the screen.
- Here are a few other really useful functions and what they do:
    - `len(string)` - Takes one argument (a string) and returns its length
    - `abs(number)` - Takes one argument (either an integer or a float) and returns its absolute value
    - `round(float)` - Takes one floating point number as an argument and rounds it to the nearest integer
    - `type(variable)` - Takes one variable as an argument and returns its type

```
# Notes 2/22/22
- python is an object oriented language
- different functions return different things
- always use parenthesis in functions to differentiate them from objects
- collections of variables in () is a touples (sp?) they cannot be changed after they are created. they can be returned as output of function. these are one type if complex data structure. 
- collections of variables in [] are lists and they can be changed. 
- len("DNA SEQUENCE") -> tells us how many nucleotides are in a sequence 
- abs(-#) returns the absolute value of the number
- round(#) rounds the number to a whole number, but the data type is still floating. 
- int(#) removes the decimals and does not round. returns integer not floating. 
- int(round(#)) nesting functions works from the inside out. 
- type(your variable) that tell you what type of variable you have (string, float, integer) 
```


## Methods
  
- Methods are functions (sort of like actions or verbs) that belong to a variable
- Methods are accessed and used by appending them to the name of a variable, separated by a `.`
- For instance, let's say we define a string - `myStr = "biOLogy  "`. Here are some really useful methods that can be used with that string:
    - `myStr.upper()` - Converts all characters in the string to uppercase
    - `myStr.lower()` - Converts all characters in the string to lowercase
    - `myStr.strip()` - Removes whitespace from the beginning or ending of the string
    - Methods can also be chained! - `myStr.strip().lower()`
    - `myStr.replace("y","ical")` - This method functions like find and replace, where the first argument is the text to find and the second argument is the text to use when replacing.
    - `myStr.split("O")` - Breaks up the string, using the character provided as an argument as the delimiter. This method then returns a list of new strings. We'll talk more about lists later.

```
# Notes 2/22/22
- the functions we decsribed exist on their own, functions that belong to specific objects are called methods. we will only want to use that function with that particular object
- we append methods to the end of the variable when we are executing them
- the example above:  `myStr = "biOLogy  "` the letters are not homogenized we want to standardize them. 
- variable.method 
    - strip: removed end space 
    - upper: uppercase
    - lower: lowercase
- we can chain methods together too, variable.method.method 
    - replace: find and replace (for a nucleotide sequence for example), we can chain them together too. this does not change the variable itself
    - store the output to a new variable using the code you ran to get the new sequence. will override the old variable though
    - join the variables using + 
    - split: breaks up the string
```

## Comments in Python

- Just like with bash, comments are essential in Python.
- Comments are included in Python by putting a `#` at the beginning of a line.
- Many text editors have a shortcut keystroke to toggle lines between being commented and uncommented. 
- `# This is an example of a comment`

## String Formatting
  
- Python has a special way to format strings so that the values of variables can be included
- The operator `%` is used to indicate that the values of certain variables should be used to fill in a string
- The parts of the string where the values should go is indicated with placeholders (kinda like wildcards)
- The three most basic placeholders are:
    - `%d` - An integer
    - `%f` - A floating point number (i.e., a decimal)
    - `%s` - A string
- Try this:
    - `faveInt = 7`
    - `faveFloat = 3.14`
    - `faveString = phyleaux`
    - `print("Favorite integer is %d, favorite float is %f, and favorite string is %s." % (faveInt,faveFloat,faveString))`
- Note how the variables holding the values are provided in the same order inside parentheses after the `%`.

```
# Notes 2/2/22
- python provides an easy to format strings when we have different variables we want to include in the string. 
- operator % tells the type of variable we want. 
- put in tuple (sp?) at the end if we want to combine them. 
```

## User Input

- Python has a special function, `input("Message:" )`, to accept input from a user.
- This function reads the user input and returns it. But be sure to store it in a variable!
    - `userStr = input("Input some string: ")`
- You can use the string methods outlined above to standardize user input - like stripping out excess whitespace, changing character case, etc.

```
Practice Exercise

Write a Python script that asks a user to input three different kinds of variables, using three 
separate input() commands. Then use string formatting to print out the values of all three 
variables in one string. Please do this in a Jupyter notebook.
```

## Getting help from Python
  
- If you need help remembering what methods are available for a given object, use `dir(<OBJECT>)`
- Note that methods starting and ending with "__" are not meant for users to call. They are methods to be used by the system.
- Try creating a string variable (e.g., `myStr = "some text"`).
    - Now run `dir(myStr)`
    - Pick a method you haven't used before and see what it does with `myStr`.

## Additional Python Resources

- [Python](https://www.python.org)
- [Software Carpentry - Intro. to Python](http://swcarpentry.github.io/python-novice-inflammation/)

```
# Notes 2/22/22
official python page, language refernce is useful. 
make sure you are reading documentation for the version of python you have. 
```
