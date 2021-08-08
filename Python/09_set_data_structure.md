# 01.08-Set Types - set

Sets: unordered, mutable, no duplicates

TABLE OF CONTENT

1. [Set](#1-set)
1. [Access Items in Set](#2-access-items-in-set)
1. [Add , remove items in Set](#3-add--remove-items-in-set)
1. [Math Operation with Set](#4-math-operation-with-set)
1. [Set Methods](#5-set-methods)
1. [Set Related functions](#6-set-related-functions)

## 1. Set

```py
# declear set
>>> thisset = {"apple", "banana", "cherry"}
>>> print(thisset)
{'cherry', 'banana', 'apple'}
>>>
```

```py
# declear set with set() function
>>> myset = set([1, 2, 3]) # set()
>>> print(myset)
{1, 2, 3}
>>> myset = set("Hello")
>>> print(myset)
{'l', 'e', 'o', 'H'}
>>> 
```

```py
# declear empty set() function
>>> myset = set()
>>> type(myset)
<class 'set'>
>>> 
```

## 2. Access Items in Set

```py
# item access with loop
>>> thisset = {"apple", "banana", "cherry"}
>>> 
>>> for x in thisset:
...   print(x)
... 
cherry
banana
apple
>>>
```

```py
# item chack with boolan 
>>> thisset = {"apple", "banana", "cherry"}
>>> 
>>> print("banana" in thisset)
True
>>>
```

## 3. Add , remove items in Set

```py
# added item
>>> myset = set()
>>> myset.add(1) # set.add()
>>> myset.add(2)
>>> myset.add(3)
>>> print(myset)
{1, 2, 3}
>>>
```

```py
# remove item
>>> myset = {1, 2, 3)
>>> myset = {1, 2, 3}
>>> myset.remove(3) # set.remove()
>>> print(myset)
{1, 2}
>>>
>>> myset.remove(4)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 4
>>>
# Note: If the item to remove does not exist, remove() will raise an error.
```

```py
# remove item using set.discard() methods
>>> myset = {1, 2, 3}
>>> myset.discard(3) # set.discard
>>> print(myset)
{1, 2}
>>> myset.discard(4)
>>>
# Note: If the item to remove does not exist, discard() will NOT raise an error.
```

```py
# set.clear() method empty set
>>> myset = {1, 2, 3}
>>> myset.clear() # set.clear()
>>> print(myset)
set()
>>> 
```

```py
>>> # set.pop() method remove item and return the removed value
>>> myset = {1, 2, 3}
>>> print(myset.pop()) # set.pop()
1
>>> print(myset)
{2, 3}
>>> 
```

## 4. Math Operation with Set

```py
# Union
>>> set1 = {"a", "b" , "c"}
>>> set2 = {1, 2, 3}
>>> 
>>> set3 = set1.union(set2) # set.union()
>>> print(set3)
{1, 2, 'a', 3, 'c', 'b'}
>>> 
```

```py
# Intersection
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> z = x.intersection(y) # set.intersection()
>>> print(z)
{'apple'}
>>> 
>>>
>>> x = {"a", "b", "c"}
>>> y = {"c", "d", "e"}
>>> z = {"f", "g", "c"}
>>> result = x.intersection(y, z) 
>>> print(result)
{'c'}
>>>
```

```py
# Difference
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> z = x.difference(y) # set.defference()
>>> print(z)
{'cherry', 'banana'}
>>> 
>>>
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> z = y.difference(x) 
>>> print(z)
{'google', 'microsoft'}
>>> 
```

```py
# Symmetric Difference
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> z = x.symmetric_difference(y) # set.symmetric_difference()
>>> print(z)
{'cherry', 'microsoft', 'google', 'banana'}
>>> 
```

## 5. Set Methods

## 6. Set Related functions

```py
# len()
>>> thisset = {"apple", "banana", "cherry"}
>>> print(len(thisset))
3
>>> 
```
