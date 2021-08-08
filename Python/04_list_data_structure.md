# List Data Structure

Python has 6 types of built-in type. These are - numeric, sequence, mapping, class, instance and exception.

There are 3 sequence types in Python: lists, tuples, and range objects.

TABLE OF CONTENT

1. [List](#1-list)
1. [2. List Slices](#2-list-slices)
1. [3. List operation , List is Mutable](#3-list-operation--list-is-mutable)
1. [4. Unpacking Lists](#4-unpacking-lists)
1. [5. Looping over List](#5-looping-over-list)
1. [6. List Methods](#6-list-methods)
1. [7. List Related functions](#7-list-related-functions)

---

## 1. List

```py
# eleyment type Roughly any in list
>>> list_items = ["Hello", 45, 88.54]
>>> print(list_items)
['Hello', 45, 88.54]
>>>
```

```py
 # 2d list
>>> matrix = [[0, 1], [2, 3]]
>>> print(matrix)
[[0, 1], [2, 3]]
>>>
```

```py
# list with range() function
>>> numbers = list(range(20))
>>> print(numbers)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
>>> 
```

```py
# length of list
>>> list_items = ["Hello", 45, 88.54]
>>> len(list_items)
3
>>> 
```

```py
# empty list
>>> my_list = []
>>> print(my_list)
[]
>>>
```

## 2. List Slices

```py
# Accessing list
>>> squares = [1, 4, 9, 16, 25]
>>> squares[0]  # indexing returns the item
1
>>> squares[1]
4
>>> squares[-1]
25
>>> squares[-2]
16
>>> 
```

```py
# Slicesing lists
>>> squares[0:3]
[1, 4, 9]
>>> squares # original list does not changes
[1, 4, 9, 16, 25]
>>> squares[:3]
[1, 4, 9]
>>> squares[1:]
[4, 9, 16, 25]
>>> copy_list = squares[:] # A copy of original list
>>> copy_list
[1, 4, 9, 16, 25]
>>>
```

```py
# advance slicesing
>>> numbers = list(range(20))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
>>> print(numbers[::1])
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
>>> print(numbers[::2])
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
>>>
>>>
>>> print(numbers[::-1]) # reverse list
[19, 18, 17, 16, 15, 14, 13, 12, 11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
>>> print(numbers[::-2])
[19, 17, 15, 13, 11, 9, 7, 5, 3, 1]
>>> 
```

## 3. List operation , List is Mutable

```py
# List is Mutable
>>> my_numbers = [1, 2, 3, 5]
>>> my_numbers[3] = 4 # can change list item
>>> print(my_numbers)
[1, 2, 3, 4]
>>> 
```

```py
# Addition and multiplication in the list
>>> squares = [1, 4, 9, 16, 25]
>>> squares + [36, 49, 64, 81, 100] # addition
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>>

>>> first_list = [1, 2, 3]
>>>first_list * 3 # multiplication
[1, 2, 3, 1, 2, 3, 1, 2, 3]
>>> 
```

```py
# Element check in list
>>> fruits = ["apple", "orange", "pineappe", "grape"]
>>> "orange" in fruits
True
>>> "rice" in fruits
False
>>> "apple" in fruits
True
>>>
>>>
>>> fruits = ["apple", "orange", "pineappe", "grape"]
>>> "orange" not in fruits # using not
False
>>> not "rice" in fruits
True
>>> 
```

## 4. Unpacking Lists

```py
>>> numbers = [1, 2, 3]
>>> first = numbers[0]
>>> second = numbers[1]
>>> third = numbers[2]
>>> print(first, second, third)
1 2 3
>>>

>>> first, second, third = numbers # useing unpacking list
>>> print(first, second, third)
1 2 3
```

```py
>>> numbers = [1, 2, 3]
>>> first, second = numbers
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: too many values to unpack (expected 2)
>>> 

>>> numbers = [1, 2, 3, 4, 5, 6, 7]
>>> first, second, *other_list = numbers
# note: Here we pack the other value in other_list
>>> print(first, second)
1 2
>>> print(other_list)
[3, 4, 5, 6, 7]
>>>

>>> first, *other_list, last = numbers
>>> print(first, last)
1 7
>>> print(other_list)
[2, 3, 4, 5, 6]
```

## 5. Looping over List

```py
>>> letters = ["a", "b", "c"] 
>>> for letter in letters:
...     print(letter)
... 
a
b
c
>>> 
```

```py
# with index
>>> for index, letter in enumerate(letters):
...     print(index, letter)
... 
0 a
1 b
2 c
>>> 
```

## 6. List Methods

There are 11 bacis mehtods in List

```py
# Add items
>>> nums = [1, 2, 3]
>>> nums.append(4) # list.append()
>>> print(nums)
[1, 2, 3, 4]
>>>

>>> words = ["A", "C"]
>>> words.insert(1, "B") # list.insert()
>>> print(words)
['A', 'B', 'C']
>>>

>>> fruits = ['apple', 'banana', 'cherry']
>>> cars = ['Ford', 'BMW', 'Volvo']
>>> fruits.extend(cars) # list.extend()
>>> print(fruits)
['apple', 'banana', 'cherry', 'Ford', 'BMW', 'Volvo']
>>> 
```

```py
# Removeing items
>>> fruits = ["apple", "banana", "cherry"]
>>> fruits.pop(1) # list.pop()
'banana'
>>> print(fruits)
['apple', 'cherry']
>>> 

>>> fruits = ["apple", "banana", "cherry"]
>>> fruits.remove("apple") # list.remove
>>> print(fruits)
['banana', 'cherry']
>>>
>>> fruits = ["apple", "banana", "cherry", "apple"]
>>> fruits.remove("apple")
>>> print(fruits)
['banana', 'cherry', 'apple']
>>> 

>>> fruits = ["apple", "banana", "cherry", "apple"]
>>> fruits.clear() # list.clear()
>>> print(fruits)
[]
>>>

>>> fruits = ["apple", "banana", "cherry", "apple"]
>>> del fruits[0:2] # del statements
>>> print(fruits)
['cherry', 'apple']
>>> 
```

```py
# Finding item

>>> letters = ['p', 'q', 'r', 's', 'p', 'u']
>>> print(letters.index('r')) # list.index()
2
>>> print(letters.index('p'))
0
>>> print(letters.index('z'))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: 'z' is not in list
>>> 

>>> letters = ['p', 'q', 'r', 's', 'p', 'u']
>>> letters.count('p') # list.count()
2
>>> 
```

```py
# reverse, sort list  and copy list
>>> fruits = ['apple', 'banana', 'cherry']
>>> fruits.reverse() # list.reverse()
>>> print(fruits)
['cherry', 'banana', 'apple']
>>>

>>> nums = [4, 2, 3, 1, 7, 9]
>>> nums.sort() # list.sort()
>>> print(nums)
[1, 2, 3, 4, 7, 9]
>>> 
>>> cars = ['Ford', 'BMW', 'Volvo']
>>> cars.sort()
>>> print(cars)
['BMW', 'Ford', 'Volvo']
>>>

>>> fruits = ["apple", "banana", "cherry"]
>>> x = fruits.copy() # list.copy
>>> print(x)
['apple', 'banana', 'cherry']
>>>
```

## 7. List Related functions

```py
# list()
>>> x = list(("apple", "banana", "cherry"))
>>> x
['apple', 'banana', 'cherry']
>>>
```

```py
# max()
>>> nums = [1, 2, 4, 20, 50, 3, 4]
>>> max(nums)
50
```

```py
# min()
>>> nums = [1, 2, 4, 20, 50, 3, 4]
>>> min(nums)
1
```

```py
# len()
>>> nums = [1, 2, 4, 20, 50, 3, 4]
>>> len(nums)
7
>>> 
```
