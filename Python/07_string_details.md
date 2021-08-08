# String Details

TABLE OF CONTENT

1. [String](#1-string)
1. [2. Strings Slicing](#2-strings-slicing)
1. [String Operation - concatenation, repetition](#3-string-operation---concatenation-repetition)
1. [String Is immutable](#4-string-is-immutable)
1. [String Related functions](#5-string-related-functions)
1. [String Methods](#6-string-methods)
1. [String Formatting - printf-style, s.format(), f-string](#7-string-formatting---printf-style-sformat-f-string)

All detail on [Python offcial Library doc](https://docs.python.org/3.8/library/stdtypes.html#text-sequence-type-str)

## 1. String

String literals are written in a variety of ways:

* Single quotes: 'allows embedded "double" quotes'
* Double quotes: "allows embedded 'single' quotes".
* Triple quoted: '''Three single quotes''', """Three double quotes"""

```py
>>> 'We love python!'  # Single Quotes
'We love python!'
>>> "We love python!"  # Double Quotes
'We love python!'
>>>
```

```py
# Triple quoted
>>> text = """
... Usage: thingy [OPTIONS]
...     -h
...     -H hostname             host name to connet to
... """
>>> print(text)

Usage: thingy [OPTIONS]
        -h
        -H hostname             host name to connet to

>>> text = """\
... Usage: thingy [Options]
...     -h
...     -H hostname             host name to connet to"""
>>> print(text)
Usage: thingy [Options]
        -h
        -H hostname             host name to connet to
>>>
```

```py
  # Split the line into chunks, which are concatenated automatically by Python
>>> text = (
... "3 little pigs come out,"
... "or I'll huff and I'll puff"
... "and I'll blow your house down.")
>>> text
"3 little pigs come out,or I'll huff and I'll puffand I'll blow your house down."
>>> print(text)
3 little pigs come out,or I'll huff and I'll puffand I'll blow your house down.
>>> 
```

* [W3 School Python Escape Characters page](https://www.w3schools.com/python/gloss_python_escape_characters.asp)

```py
# Escape sequences
# \"
# \'
# \\
# \n

>>> course = 'Python "Programming'
>>> print(course)
Python "Programming
>>>
>>> course = "Python \"Programming" # \:
>>> print(course)
Python "Programming
>>> 

>>> course = "python 'Programming"
>>> print(course)
python 'Programming
>>> 
>>> course = "Python \'Programming" # \'
>>> print(course)
Python 'Programming
>>>
'
>>> course = "Python \nProgramming" # \n
>>> print(course)
Python 
Programming
>>> 
>>> print('C:\some\name')  # here \n means newline!
C:\some
ame
>>> print(r'C:\some\name')  # note the r before the quote
C:\some\name
>>>

>>> course = "python \programming"
>>> print(course)
python \programming
>>> 
>>> course = "Python \\Programming" # \\
>>> print(course)
Python \Programming
>>> 
```

## 2. Strings Slicing

```py
>>> word = 'Python'
>>> word[0]  # character in position 0
'P'
>>> word[5]  # character in position 5
'n'
```

```py
>>> word[-1]  # last character
'n'
>>> word[-2]  # second-last character
'o'
>>> word[-6]
'P'
```

```py
# %d int, %s string, %f/%g floating 
>>> word[0:2]  # characters from position 0 (included) to 2 (excluded)
'Py'
>>> word[2:5]  # characters from position 2 (included) to 5 (excluded)
'tho'
```

```py
>>> word[:2] + word[2:] # concatenate
'Python'
>>> word[:4] + word[4:]
'Python'
```

```py
>>> word[:2]   # character from the beginning to position 2 (excluded)
'Py'
>>> word[4:]   # characters from position 4 (included) to the end
'on'
>>> word[-2:]  # characters from the second-last (included) to the end
'on'

 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1

>>> word[4:42]
'on'
>>> word[42:]
''
```

## 3. String Operation - concatenation, repetition

```py
# String Concatenation
>>> "Spam" + 'eggs'
'Spameggs'

>>> print("First string" + ", " + "second string")
First string, second string

>>> "2" + "2"
'22'

>>> 'Py' 'thon' # Automatically concatenated
'Python'

>>> prefix = "Py"
>>> prefix + 'thon'
'Python'

>>> 1 + '2' + 3 + '4'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'

```

```py
# String Repetition
>>> print("spam" * 3)
spamspamspam

>>> 4 * '2'
'2222'

>>> '17' * '87'
TypeError: can't multiply sequence by non-int of type 'str'

>>> 'pythonisfun' * 7.0
TypeError: can't multiply sequence by non-int of type 'float'
```

## 4. String Is immutable

```py
>>> word[0] = 'J'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> word[2:] = 'py'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```

```py
>>> 'J' + word[1:] # if need a different string, crate a new one
'Jython'
>>> word[:2] + 'py'
'Pypy'
```

## 5. String Related functions

```py
# len() function
>>> s = 'supercalifragilisticexpialidocious'
>>> len(s)
34
>>>
```

```py
# str() Function
>>> integer = 54
>>> int_to_str = str(integer)
>>> int_to_str
'54'

>>> float = 34.2342
>>> float_to_str = str(float)
>>> float_to_str
'34.2342'
>>> 
```

## 6. String Methods

Note: All string methods returns new values. They do not change the original string. Becuase string is Immutable

```py
# s.upper(), s.lower() and s.title()
>>> print("This is a sentence.".upper())
THIS IS A SENTENCE.
>>>

>>> print("AN ALL CAPS SENTENCE".lower())
an all caps sentence
>>>

>>> full_name = "shihab mahamud"
>>> print(full_name.title())
Shihab Mahamud
>>> 
```

```py
# s.strip(), s.lstrip() and s.rstrip()
>>> s = "  I love Allah  "
>>> s
'  I love Allah  '
>>> s.strip()
'I love Allah'

>>> s.lstrip()
'I love Allah  '

>>> s.rstrip()
'  I love Allah'

>>> s # this above method return new String
'  I love Allah  ' 
>>>
```

```py
# s.find(sub_str)
>>> text = "Hello, welcome to house"
>>> text.find("e")
1
>>> text.find("ello")
1
>>> text.find("wel")
7

>>> text.find("e", 5, 10) # find between 5 to 10
8

>>> text.find("q") # if not found return -1
-1
>>>
```

```py
# s.replace('old', 'new') 
>>> print("Hello ME".replace("ME", "world"))
Hello world

>>> text = "I Like bananas"
>>> text.replace("bananas", "apples")
'I Like apples"
>>> text
'I Like bananas'

>>> text = "one one was a race horse, two two was one too."
>>> text.replace("one", "three")
'three three was a race horse, two two was three too.'

>>> text = "one one was a race horse, two two was one too."
>>> text.replace("one", "three",2) # replace with specific range
'three three was a race horse, two two was one too.'
>>> 
```

```py
# s.isalpha() , isdigit(), isspace() ... methods
>>> s = "Bangladesh" # s.isalpha()
>>> s.isalpha()
True
>>> s = "66"
>>> s.isalpha()
False
>>> 

>>> s.isdigit() # s.isdigit()
True
>>> s = "Bangladesh"
>>> s.isdigit()
False

>>> s = "  " # s.isspace()
>>> s.isspace()
True
>>> s = "Bangladesh"
>>> s.isspace()
False
>>> 

>>> s = "Bangladesh 55"
>>> s.isdigit()
False
>>> s.isalpha()
False
>>> s.isspace()
False
>>>

More:-
          isalnum(), isalpha(), isdecimal()
          isidentifier(), islower(), isnumeric(),
          isprintable(), istitle(), isupper()

Total 11 methods

```

```py
# s.startswith(sub_str) and s.endswith(sub_str)
>>> print("This is a sentence.".startswith("This"))
True
>>> print("This is a sentence.".endswith("sentence."))
True
>>>
```

```py
# s.split('delim')
print("a, e, i, o, u".split(", "))
['a', 'e', 'i', 'o', 'u']

>>> text = "welcome to the jungle"
>>> x = tet.split()
>>> print(x)
['welcome', 'to', 'the', 'jungle']

>>> text = "hello, my name is Peter, I am 26 years old"
>>> x = txt.split(", ")
>>> print(x)
['one one was a race horse', 'two two was one too.']

>>> txt = "apple#banana#cherry#orange"
>>> x = txt.split("#")
>>> print(x)
['apple', 'banana', 'cherry', 'orange']

>>> txt = "apple#banana#cherry#orange#good"
# setting the maxsplit parameter to 1, will return a list with 3 elements!
>>> x = txt.split("#", 2)
>>> print(x)
['apple', 'banana', 'cherry#orange#good']
>>>
```

```py
# s.join(list) 
>>> print(", ".join(["apple", "orange", "pineapple"])) # list to str
apple, orange, pineapple
>>> myTuple = ("John", "Peter", "Vicky")
>>> x = "#".join(myTuple)
>>> print(x)
'John#Peter#Vicky'

>>> myDict = {"name": "John", "country": "Norway"} # dictionay to str
>>> mySeparator = "TEST"
>>> x = mySeparator.join(myDict)
>>> print(x)
nameTESTcountry
>>>
```

```py
# s.index(sub_str)
>>> txt = "Hello, welcome to my world."
>>> x = txt.index("welcome")
>>> print(x)
7

>>> txt = "Hello, welcome to my world."
>>> x = txt.index("e", 5, 10)
>>> print(x)
8

>>> txt = "Hello, welcome to my world."
>>> print(txt.find("q")) # find return -1
-1
>>> print(txt.index("q")) # index gave error
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>>
```

There are 44 String methods in python.
For more:-

* [W3 School string Methods page](https://www.w3schools.com/python/python_ref_string.asp)
* [Python offcial Libaray String Methods page](https://docs.python.org/3.8/library/stdtypes.html#string-methods)

## 7. String Formatting - printf-style, s.format(), f-string

```py
# printf-style formatting  # %d int, %s string, %f/%g floating 
>>> text = "%d little pigs come out, or I'll %s, and I'll %s, and I'll blow your %s down."%(3, 'huff', 'puff', 'house')
>>> text
"3 little pigs come out, or I'll huff, and I'll puff, and I'll blow your house down."
>>> 
```

```py
# s.format() 
>>> msg = "My self score on PHP: {0}, Python: {1}, Java: {2}, Swift: {3}". format(6, 6.5, 5, 6)
>>> print(msg)
My self score on PHP: 6, Python: 6.5, Java: 5, Swift: 6
>>>
>>> '{2}, {1}, {0}'.format('a', 'b', 'c')
'c, b, a'
>>> '{0}{1}{0}'.format('abra', 'cad')
'abracadabra'
>>>
>>> message = "If x={x} and y={y}, then x+y={z}".format(x = 20, y = 300, z = 20+300)
>>> print(message)
If x = 20 and y = 300, then x+y = 320
>>>
```

```py
# f-String
# Support Python version =>3.6
>>> first = "Shihab"
>>> last = "Mahamud"
>>> full = f"Name: {first} {last}"
>>> print(full)
Name: Shihab Mahamud
>>> full= f"{len(first)} {2+2}"
>>> print(full)
6 4
>>> 
```

See also:

* [Google developers python Strings doc](https://developers.google.com/edu/python/strings)
* [Python offcial String doc](https://docs.python.org/3.8/tutorial/introduction.html#strings)
* [How to code bangla String page](https://python.howtocode.dev/basic-concept/string-operations)
* [W3 School String page](https://www.w3schools.com/python/python_strings.asp)
