# Introduction to Python: Fundamentals (DEV274x)

## Module 1: Sequence index

```python
# Accessing a single string character
string = "abcdef"
string[0]   # a
string[2]   # c
string[-1]  # f

# Index slicing
# string[start:stop:step]
string[1:3]     # bc
string[1:]      # bcdef
string[:3]      # abc
string[::2]     # ace
string[::-1]    # fedcba
string[3:0:-1]  # dcb

# Iterate through strings letter by letter
for letter in string:
    print(letter)

# Get length of a string
len(string)     # 6

# Count occurances in a string
"My sentence".count("e")        # 3
"My sentence".count("sentence") # 1

# Find occurance in a string
# If multiple occurances, returns first one. If none, returns -1
"My sentence".find("e")         # 4
"My sentence".find("sentence")  # 3
"My sentence".find("avocado")   # -1
```

## Module 2: Sequence manipulation

``` python
# Creating lists (preserves order, can have duplicates and multiple types)
emptylist = []
numberlist = [1, 2, 3, 4, 5, 5, 5]
mixedlist = [1, 2, "hello", 3.14, [1, 2, 3]]

# Accessing lists
numberlist[3]   # 4
mixedlist[0]    # 1
mixedlist[4][2] # 3

# Editing lists
numberlist[3] = 177
numberlist      # [1, 2, 3, 177, 5, 5, 5]

# Appending to lists
emptylist.append(6)
emptylist.append("hi")
emptylist       # [6, 'hi']

# Inserting into lists
# list.insert(index, elem)
# list[index] = elem, everything else shifted along
emptylist.insert(1, "hello")
emptylist       # [6, 'hello', 'hi']

# Remove elements at an index from a list
del emptylist[1]
emptylist       # [6, 'hi']

# Remove and return the last element from a list
numberlist.pop()    # 5
# Remove and return elements at an index from a list
numebrlist.pop(1)   # 2
numberlist          # [1, 3, 177, 5, 5]

# Remove the 1st element that matches from a list
# Will throw ValueError if not in the list
mixedlist.remove(3.14)
mixedlist           # [1, 2, "hello", [1, 2, 3]]

# In a conditional, an empty list will evaluate False
while emptylist:
    print(emptylist.pop())
print(emptylist)    # []
```

## Module 3: Sequence iteration

```python
# Iterate through lists using for x in list
visited = ["New York", "Shanghai", "Munich"]
for city in visited:
    print(city)

# range(start, stop, step) iteration
list(range(3))      # [0, 1, 2]
list(range(3, 7))   # [3, 4, 5, 6]
list(range(2,8,2))  # [2, 4, 6]

# Combine lists
wishlist = ["London", "Paris"]
# in place
visited.extend(wishlist)
visited     # ['New York', 'Shanghai', 'Munich', 'London', 'Paris']
# not in place (visited & wishlist not modified)
allcities = visited + wishlist
allcities   # ['New York', 'Shanghai', 'Munich', 'London', 'Paris']

# Reverse a list
# in place
allcities.reverse()
# not in place (allcities not modified)
allcitiesbackwards = allcities[::-1]

# Sort a list
# in place
allcities.sort()
# not in place (allcities not modified)
allcitiessorted = sorted(allcities)

# Converting a string to a list with .split()
"This is a lot of words".split()
    # ['This', 'is', 'a', 'lot', 'of', 'words']
"How much for the dog in the window".split("o")
    # ['H', 'w much f', 'r the d', 'g in the wind', 'w']

# Building a string from a list
" ".join(["Hello", "world"])    # 'Hello world'
"**".join(["A", "d", "a", "m"]) # 'A**d**a**m'

# Cast a string to a list
list("Adam")    # ['A', 'd', 'a', 'm']

# Changing the end parameter of print()
print("Hello", end="!!!\n")
# Hello!!!
# 
```

## Module 4: Files

```python
# Import files into Jupyter via curl
!curl https://pastebin.com/raw/6i6mkDEx -o poem1.txt

# Open file in read mode
poem_file = open('poem1.txt', 'r')

# Read contents of a file (returns a string)
poem_contents = poem_file.read()

# Read a number of characters
first10char = poem_file.read(10)

# Read contents as a file as lines, including the \n's
# Returns a list of strings
poem_lines = poem_file.readlines()

# Read one line at a time (returns a string, including \n)
poem_file.readline()

# Close a file
poem_file.close()

# string.strip(characters) removes leading and trailing characters
# Defualt is all whitespace, including \n
"  test string!  \t\n".strip()  # 'test string!'
"*+*++Aug+ust*+*".strip("*+")   # 'Aug+ust'

# Opening a file in write mode
# Will create new file or overwrite existing
new_file = open('new_file.txt', 'w')

# Opening a file in write plus read mode
# Will create new file or overwrite existing
new_file = open('new_file.txt', 'w+')
new_file.write("Hello World!\n")

# file.seek(index) moves the file pointer to the index
new_file.seek(0)
new_file.read() # 'Hello World!\n'
```

`file.seek(index, whence_mode)` moves the file pointer to the index dependent on the whence mode

| whence_mode 	| description                                        	|
|-------------	|----------------------------------------------------	|
| 0           	| points to the beginning of the file                	|
| 1           	| points to the current location                     	|
| 2           	| points to the end of the file & offset is always 0 	|

`file = open(filename, mode)` opens files

| mode 	| Description                                                 	|
|------	|-------------------------------------------------------------	|
| 'r'  	| read only mode                                              	|
| 'w'  	| write - overwrites file with same name                      	|
| 'w+' 	| write and read mode - overwrites file with same name        	|
| 'r+' 	| read and write mode (no overwrite)                          	|
| 'a'  	| opens for appending to end of file (no overwrite)           	|
| 'a+' 	| opens for appending to end of file (no overwrite) plus read 	|