# Data Types

3 basic data types in python int, float, str

TABLE OF CONTENT

1. [Integer](#1-integer)
1. [Floating Point](#2-floating-point)
1. [String](#3-string)
1. [Type Conversion](#type-conversion)

## 1. Integer

```py
>>> x = 1
>>> y = 35656222554887711
>>> z = -3255522
>>> x
1
>>> y
35656222554887711
>>> z
-3255522
>>> print(type(x), type(y), type(z))
<class 'int'> <class 'int'> <class 'int'>
>>>
```

## 2. Floating Point

```py
>>> x = 1.10
>>> x
1.1
>>> y = 1.0
>>> y
1.0
>>> z = -35.59
>>> z
-35.59
>>> print(type(x), type(y), type(z))
<class 'float'> <class 'float'> <class 'float'>
>>> 
```

```py
# Float can also be scientific numbers with an "e" to indicate the power of 10.
>>> x = 35e3
>>> print(x)
35000.0
>>> y = 12E4
>>> print(y)
120000.0
>>> z = -87.7e100
>>> print(z)
-8.77e+101
>>> print(type(x), type(y), type(z))
<class 'float'> <class 'float'> <class 'float'>
>>> 
```

## 3. String

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

[String all details](https://google.com)

## Type Conversion

```py

# convert from int to float
>>> x_int = 1
>>> x_float = float(x_int) # float()
>>> x_int
1
>>> x_float
1.0
>>> print(type(x_int), type(x_float))
<class 'int'> <class 'float'>
>>>
```

```py
#convert from float to int:
>>> y_float = 2.8
>>> y_int = int(y_float) # int()
>>> y_float
2.8
>>> y_int
2
>>> print(type(y_float), type(y_int))
<class 'float'> <class 'int'>
>>> 
```

```py
# Convert str to int
>>> s = "445"
>>> a = int(s)
>>> a
445
>>> type(a)
<class 'int'>
>>>
```

```py
# Convert str to float
>>> s = "5.323"
>>> f = float(s)
>>> f
5.323
>>> type(f)
<class 'float'>
>>> 

```

```py
# Convert int ot str
>>> x = str(2)
>>> x
'2'
>>> type(x)
<class 'str'>
```

```py
# Convert float to str
>>> y = str(3.0)
>>> y
'3.0'

>>> type(y)
<class 'str'>
>>>
```
