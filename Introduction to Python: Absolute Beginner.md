# Introduction to Python: Absolute Beginner (DEV236x)

## Module 1: Basics

The Jupyter Notebooks is a web app that allows you to write and run Python code in code cells, and write markdown in markdown cells.

```python
# This is a comment

# Printing strings
print("Hello World!")

# A string is a sequence of characters
string1 = 'as long as they match, single or'
string2 = "double quotes work to make strings"

# Integers are whole numbers
int1 = 3
int2 = -314

# Floats have decimal places
float1 = 2.72
float2 = 6.0

# You can find out the type of a variable with type()
type("Hello")   # <class 'str'>
type(3)         # <class 'int'>
type(3.0)       # <class 'float'>

# Python variables can change the type of data a variable holds
variable = 999
variable = "I'm a string now"

# Addition
42 + 10         # 52
"Hi " + "world" # "Hi world"

# Errors
"hi" + 42       # TypeError: str and int are different types
print("open"    # SyntaxError: missing closing parenthesis
print(x)        # NameError: x is not defined

# Casting
"hi" + str(42)  # "hello42"

# Getting user input
name = input("Enter name: ")

# Printing strings and numbers without casting
print("My name is", name, "and I'm on module", 1, "and my favourite number is", 3.14)

# Boolean string methods
string.isalpha()
string.isalnum()
string.istitle()
string.isdigit()
string.islower()
string.isupper()
string.startswith(string2)

# String format methods
string.capitalize()
string.lower()
string.upper()
string.swapcase()
string.title()

# Boolean in keyword
"Hello" in "Hello world"

```

## Module 2: Functions

```python
# Calling functions
function_name(arg1, arg2)

# Defining a function
def function_name(param1, param2):
    # Returning a value
    return param1 + param2

# Defining a function with default arguments
def say_hello(towards = "world"):
    print("Hello " + towards + "!")
```

Arguments are the values passed into the function.

Parameters are the placeholders that will take the arguments values.

Sequence refers to the order that code is processed. Objects in Python are not available until they have been processed. Therefore function definitions are usually placed at the beginning of a piece of code.

If a function is called before it is defined, it will result in a `NameError`.

You should avoid 'hard-coding', or using literals, where possible. It makes it easier to convert functions to be general purpose, and allows functions to use configuration files or user input.

## Module 3: Conditionals

```python
# If / elif / else
if isRaining():
    print("Definitely bring your umbrella")
elif isCloudy():
    print("You should probably bring your umbrella")
else:
    print("Don't bother bringing you umbrella")

# Comparison operators
7 <   8     # true
4 >   3     # true
6 <=  5     # false
4 >= 2.6    # true
8 == 8.0    # true
1 !=  1     # false

# Comparing strings works with the above operators (based off ASCII)
"g" > "a"   # true
"z" < "A"   # false
"ba" < "bb" # true
"h" == "h"  # true

# Maths
3 + 4 # 7
3 - 4 # -1
3 * 4 # 12
3 / 4 # 0.75

# Whenever doing maths on a float, will return with a float
3 + 3.0 # 6.0
# Whenever dividing, will return a float
3 / 3   # 1.0
# Otherwise will be int

# Floored division
# Equivalent to int(a/b)
# Will drop numbers after decimal point
14 / 5  # 2.8
14 // 5 # 2
```

## Module 4: Nesting and Loops

```python
# Nested conditional
if isRaining():
    if haveUmbrella():
        print(":)")
    else:
        print(":(")
else
    print(":)")

# Escape sequences
print("This string has \"quotes\", backslashes \\\\, and \nnewlines")
# This string has "quotes", backslashes \\, and
# newlines

# While true loop
while True:
    attempt = input("Enter password: ")
    if attempt == "1234":
        print("Access granted")
        # Break
        break
    else:
        print("Acess denied")

# Incrementing and decrementing variables
incrementme = incrementme + 1
incrementme += 1
decrementme = decrementme - 1
decrementme -= 1
# There are no ++ or -- operators

# While boolean loop
i = 5
while i > 0:
    print(i)
    i -= 1
# 5, 4, 3, 2, 1

# While boolean loop with strings
name = ""
while name.isalpha() == False:
    name = input("First name: ")
```
