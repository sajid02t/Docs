# Conditional Logic

TABLE OF CONTENT

1. [Comparison Operators](#comparison-operators)
1. [if, elif, else statement](#if-elif-else-statement)
1. [Logical Operators](#logical-operators)

## Comparison Operators

```py
>>> 2 == 3 #Equal
False
>>> 3 == 3
True
>>>
```

```py
>>> 2 != 3 #Not equal
True
>>> 3 != 3
False
>>>
```

```py
>>> 2 > 3 #Greater than
False
>>>
```

```py
>>> 2 < 3 #Less than
True
>>> 
```

```py
>>> 2 >= 3 #Greater than or equal to
False
>>>
```

```py
>>> 2 <= 3 #Less than or equal to
True
>>> 
```

## if, elif, else statement

```py
>>> a = 33
>>> b = 33
>>> if b > a:
...   print("b is greater than a")
... elif a == b:
...   print("a and b are equal")
... 
a and b are equal
>>>
```

## Logical Operators

```py
# and operator
>>> x = 5
>>> x > 3 and x < 10
True
>>> 
>>> a = 200
>>> b = 33
>>> c = 500
>>> if a > b and c > a:
...   print("Both conditions are True")
... 
Both conditions are True
>>> 
```

```py
# or operator
>>> x = 5
>>> x > 3 or x < 4
True
>>> a = 200
>>> b = 33
>>> c = 500
>>> if a > b or a > c:
...   print("At least one of the conditions is True")
... 
At least one of the conditions is True
>>>
```

```py
>>> x = 5
>>> 
>>> not(x > 3 and x < 10)
False
>>> 
>>> # returns False because not is used to reverse the result
>>> 
```
