# Tuple Date Structure

TABLE OF CONTENT

1. [Tuple](#1-tuple)
1. [Tuple Slices](#2-tuple-slices)
1. [Pack and Unpack Tuple](#3-pack-and-unpack-tuple)
1. [Tuple is Immutable](#4-tuple-is-immutable)
1. [Tuple Methods](#5-tuple-methods)
1. [Tuple Related functions](#6-tuple-related-functions)

## 1. Tuple

```py
# declear tuple
>>> x = (1, 2, 3)
>>> type(x) '''
<class 'tuple'>
>>> '''
```

```py
# declear tuple without Parenthesis
>>> x = 1, 2, 3
>>> type(x) '''
<class 'tuple'>
>>> '''
```

```py
# declear only one items in tuple
>>> x = 1
>>> type(x) '''
<class 'int'> '''
>>> x = 1,
>>> type(x) '''
<class 'tuple'> '''
```

```py
# empty tuple
>>> t = ()
>>> type(t)
<class 'tuple'>
>>> 
```

## 2. Tuple Slices

```py
# Access Tuple Items
>>> thistuple = ("apple", "banana", "cherry")
>>> thistuple[1]
'banana'
>>> thistuple[-1]
'cherry'
>>> thistuple[-2]
'banana'
>>>
```

```py
# Slices Tuple
>>> thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
>>> thistuple[2:5]
('cherry', 'orange', 'kiwi')
>>> thistuple[-4:-1]
('orange', 'kiwi', 'melon')
>>>
```

## 3. Pack and Unpack Tuple

```py
# unpack tuple
>>> numbers = (10, 20, 30, 40)
>>> n1, n2, n3, n4 = numbers
>>> n1
10
>>> n2
20
>>> n3
30
>>> n4
40
>>>
```

```py
# pack tuple
>>> n3 = 30
>>> n4 = 40
>>> t = n3 , n4
>>> t
(30, 40)
>>>
```

## 4. Tuple is Immutable

```py
# tuple is immutable
>>> tpl = (1, 2, 3)
>>> tpl
(1, 2, 3)
>>> tpl[0] = 5
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
>>> 
```

## 5. Tuple Methods

```py
# tuple.count()
>>> thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
>>> x = thistuple.count(5)
>>> x
2
>>> 
```

```py
# tuple.index()
>>> thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
>>> thistuple.index(8)
3
>>> 
```

## 6. Tuple Related functions

```py
# len()
>>> thistuple = ("apple", "banana", "cherry")
>>> len(thistuple)
3
>>> 
```

```py
# tuple to list - list()
>>> tpl = (1, 2, 3)
>>> li = list(tpl)
>>> li
[1, 2, 3]
>>>
```
