# Dictonary Data Structure

Dictionary: Key-Value pairs, Unordered, Mutable

TABLE OF CONTENT

1. [Dictionary](#1-dictionary)
1. [Accessing, Changing, Adding items](#2-accessing-changing-adding-items)
1. [Removing Items](#3-removing-items)
1. [Loop Through a Dictionary](#4-loop-through-a-dictionary)
1. [Copy a Dictionary](#5-copy-a-dictionary)
1. [Dictionary Mathods](#6-dictionary-mathods)
1. [Dictionary Related functions](#7-dictionary-related-functions)

## 1. Dictionary

```py
# declear dictionary
>>> mydict = {"name": "Shihab", "age": 18, "city": "Faridpur"}
>>> print(mydict)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur'}
>>>
```

```py
# dict() function also give same result
>>> mydict2 = dict(name="Shihab", age=18, city="Faridpur")
>>> print(mydict2) # dict()
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur'}
>>>
# Anything that is not mutable in the dictionary can be used as a key. Such as: numbers, strings, tuples. But lists,
# sets cannot be used, because lists are mutable, meaning they can be changed.
```

## 2. Accessing, Changing, Adding items

```py
# Accessing Items
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> x = thisdict["model"]
>>> print(x)
Mustang
>>>
# dict.get() also give same result
>>> x = thisdict.get("model") # dict.get()
>>> print(x)
Mustang
>>> 
```

```py
# Changing items
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> print(thisdict)
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
>>>
>>> thisdict["year"] = 2018
>>> print(thisdict)
{'brand': 'Ford', 'model': 'Mustang', 'year': 2018}
>>> 
```

```py
# Adding items
>>> mydict = {"name": "Shihab", "age": 28, "city": "Faridpur"}
>>> print(mydict)
{'name': 'Shihab', 'age': 28, 'city': 'Faridpur'}
>>>
>>> mydict["email"] = "shihab@xyz.com"
>>> print(mydict)
{'name': 'Shihab', 'age': 28, 'city': 'Faridpur', 'email': 'shihab@xyz.com'}
>>> 
```

## 3. Removing Items

```py
# using dict.pop() method
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> thisdict.pop("model") # dict.pop()
'Mustang'
>>> print(thisdict)
{'brand': 'Ford', 'year': 1964}
>>>
```

```py
# dict.popitem() method delete last item
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> thisdict.popitem() # dict.popitem()
('year', 1964)
>>> print(thisdict)
{'brand': 'Ford', 'model': 'Mustang'}
>>>
```

```py
# del statments
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> del thisdict["model"]
>>> print(thisdict)
{'brand': 'Ford', 'year': 1964}
>>> 
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> del thisdict
>>> print(thisdict) #this will cause an error because "thisdict" no longer exists.
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'thisdict' is not defined
>>>
```

```py
# The clear() method empties the dictionary:
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> thisdict.clear() #dict.clear()
>>> print(thisdict)
{}
>>> 
```

## 4. Loop Through a Dictionary

```py
# Return keys
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> for x in thisdict:
...   print(x)
... 
brand
model
year
>>>
# using dict.keys() method return keys
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> for key in thisdict.keys(): # dict.keys()
...     print(key)
... 
brand
model
year
>>> 
```

```py
# Return Values
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> for x in thisdict:
...   print(thisdict[x])
... 
Ford
Mustang
1964
>>>
# using dict.values() method return values
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> for x in thisdict.values(): # dict.values()
...   print(x)
... 
Ford
Mustang
1964
>>> 
```

```py
# Return keys, values togather using dict.items() method
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> for x, y in thisdict.items():
...   print(x, y)
... 
brand Ford
model Mustang
year 1964
>>>
```

## 5. Copy a Dictionary

```py
# without dict.copy() method
>>> mydict = {"name": "Shihab", "age": 18, "city": "Faridpur"}
>>> print(mydict)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur'}
>>> mydict_cpy = mydict # it change the original dictionary
>>> mydict_cpy["email"] = "shihab@ok.com" 
>>> print(mydict_cpy)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur', 'email': 'shihab@ok.com'}
>>> print(mydict)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur', 'email': 'shihab@ok.com'}
>>> 
```

```py
# with dict.copy() method
>>> mydict = {"name": "Shihab", "age": 18, "city": "Faridpur"}
>>> mydict_cpy = mydict.copy() # dict.copy()
>>> mydict_cpy["email"] = "shihab@ok.com"
>>> print(mydict_cpy)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur', 'email': 'shihab@ok.com'}
>>> print(mydict)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur'}
>>> 
```

```py
# with dict() function 
>>> mydict = {"name": "Shihab", "age": 18, "city": "Faridpur"}
>>> mydict_cpy = dict(mydict) # dict()
>>> mydict_cpy["email"] = "shihab@ok.com"
>>> print(mydict_cpy)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur', 'email': 'shihab@ok.com'}
>>> print(mydict)
{'name': 'Shihab', 'age': 18, 'city': 'Faridpur'}
>>>
```

## 6. Dictionary Mathods

```py
# dict.clear()
# See in '3. Removing Items' section
```

[3. Removing Items](#3-removing-items)

```py
# dict.copy() 
# See in '5. Copy a Dictionary' section
```

[5. Copy a Dictionary](#5-copy-a-dictionary)

```py
# dict.fromkeys
# Create a dictionary with 3 keys, all with the value 0:
>>> x = ('key1', 'key2', 'key3')
>>> y = 0
>>> thisdict = dict.fromkeys(x, y)
>>> print(thisdict)
{'key1': 0, 'key2': 0, 'key3': 0}
>>>

>>> x = ('key1', 'key2', 'key3')
>>> thisdict = dict.fromkeys(x)
>>> print(thisdict)
{'key1': None, 'key2': None, 'key3': None}
>>> 
```

```py
# dict.get()
# See in '2. Accessing, Changing, Adding items' section
```

[2. Accessing, Changing, Adding items](#2-accessing-changing-adding-items)

```py
# dict.items()
# See in '4. Loop Through a Dictionary' section
```

[4. Loop Through a Dictionary](#4-loop-through-a-dictionary)

```py
# dict.keys()
# See in '4. Loop Through a Dictionary' section
```

[4. Loop Through a Dictionary](#4-loop-through-a-dictionary)

```py
# dict.pop()
# See in '3. Removing Items' section
```

[3. Removing Items](#3-removing-items)

```py
# dict.popitem()
# See in '3. Removing Items' section
```

[3. Removing Items](#3-removing-items)

```py
# dict.setdefault()
>>> car = {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> x = car.setdefault("model", "Bronco")
>>> print(x)
Mustang
>>>

# Get the value of the "color" item, if the "color" item does not exist, insert "color" with the value "white":
>>> car = {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> x = car.setdefault("color", "White")
>>> print(x)
White
>>> 
```

```py
# dict.update()
>>> my_dict = {"name":"Max", "age":28, "email":"max@xyz.com"}
>>> my_dict_2 = dict(name="Mary", age=27, city="Boston")
>>> my_dict.update(my_dict_2)
>>> print(my_dict)
{'name': 'Mary', 'age': 27, 'email': 'max@xyz.com', 'city': 'Boston'}
>>> 
```

```py
# dict.values()
# See in '4. Loop Through a Dictionary' section
```

[4. Loop Through a Dictionary](#4-loop-through-a-dictionary)

## 7. Dictionary Related functions

```py
# dict()
# See in '1. Dictionary' section
```

[1. Dictionary](#1-dictionary)

```py
# len()
>>> thisdict =  {
...   "brand": "Ford",
...   "model": "Mustang",
...   "year": 1964
... }
>>> 
>>> print(len(thisdict))
3
>>> 
```
