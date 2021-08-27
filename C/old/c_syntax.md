# The C Programming Language

TABLE OF CONTENT


1. [Character sets, Keywords and Identifiers](#1-character-sets-keywords-and-indentifiers)
    1. [Character sets of C](#1-character-sets-of-c)
    2. [C Keywords](#2-c-keywords)
    3. [Rules for an Identifier](#3-rules-for-an-identifier)
    4. [Ascii Code](#4-ascii-code)
2. [Data Types](#4-data-types)
    1. [Integer Types](#1-integer-types)
    2. [Floting Point Number](#2-floting-point-number)
    3. [Character Types](#3-character-types)
3. [Operator](#3-operator)

---

## 1. Character sets, Keywords and Identifiers
### 1. Character sets of C
The characters in C are grouped into the following two categories:
* Source character set
    1. Alphabets:-

        Uppercase letters:    `A-Z`<br>
        Lowercase letters:    `a-z`
    2. Digits:-

        `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`
    3. Special Characters:-

        `~   %   |   @   +   <   _   -   >   ^`<br>
        `#   =   &   $   /   (   *   \   )   ′`<br>
        `:   [   "   ;   ]   !   ,   {   ?   }`
    4. White Spaces:-

        ` \b  \t  \v  \r  \f  \n  \\  \’  \"  \?`<br>
        `\0  \a `
* Execution character set
    1. Escape Sequence:-
		
		`\a  \b  \f  \n  \r  \t  \v  \\  \'  \?`<br>
        `\ooo    \xhh    \0`
		

### 2. C Keywords

Details: https://en.cppreference.com/w/c/keyword 

<table>
<tbody>
<tr>
<td>

* [ ] `auto`  
* [x] `break`  
* [x] `case`  
* [x] `char`  
* [ ] `const`  
* [x] `continue`  
* [ ] `default`  
* [ ] `do`  
* [x] `double`  
* [x] `else`  
* [ ] `enum`  
* [ ] `extern`
</td>
<td>

* [x] `float`  
* [x] `for`  
* [ ] `goto`  
* [x] `if`  
* [ ] `inline` <span>(since C99)</span>  
* [x] `int`  
* [x] `long`  
* [ ] `register`  
* [ ] `restrict` <span>(since C99)</span>  
* [x] `return`  
* [x] `short`
</td>
<td>

* [x] `signed`  
* [x] `sizeof`  
* [ ] `static`  
* [ ] `struct`  
* [x] `switch`  
* [x] `typedef`  
* [ ] `union`  
* [x] `unsigned`  
* [x] `void`  
* [ ] `volatile`  
* [x] `while`
</td>
<td>

* [ ] `_Alignas` <span>(since C11)</span>  
* [ ] `_Alignof` <span>(since C11)</span>  
* [ ] `_Atomic` <span>(since C11)</span>  
* [ ] `_Bool` <span>(since C99)</span>  
* [ ] `_Complex` <span>(since C99)</span>  
* [ ] `_Decimal128` <span>(since C23)</span>
* [ ] `_Decimal32` <span>(since C23)</span>
* [ ] `_Decimal64` <span>(since C23)</span>
* [ ] `_Generic`<span>(since C11)</span>  
* [ ] `_Imaginary` <span>(since C99)</span>  
* [ ] `_Noreturn` <span>(since C11)</span>  
* [ ] `_Static_assert`s <span>(since C11)</span>  
* [ ] `_Thread_local` <span>(since C11)</span>
</td>
</tr>
</tbody>
</table>

### 3. Rules for an Identifier

1. An Identifier can only have alphanumeric characters`(a-z , A-Z , 0-9)` and underscore`(_)`.
2. The first character of an identifier can only contain alphabet`(a-z , A-Z)` or underscore `(_)`.
3. Identifiers are also case sensitive in C. For example name and Name are two different identifiers in C.
4. Keywords are not allowed to be used as Identifiers.
5. No special characters, such as semicolon, period, whitespaces, slash or comma are permitted to be used in or as Identifier.

### 4. Ascii Code

### ASCII Table

| Dec  | Hex  | Oct  | Html   | Char  | Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- | :--- | :--- | :--- | :----- | :---- |
| 0    | 0    | 000  |        | NUL   | 11   | B    | 013  |        | VT    |
| 1    | 1    | 001  |        | SOH   | 12   | C    | 014  |        | FF    |
| 2    | 2    | 002  |        | STX   | 13   | D    | 015  |        | CR    |
| 3    | 3    | 003  |        | ETX   | 14   | E    | 016  |        | SO    |
| 4    | 4    | 004  |        | EOT   | 15   | F    | 017  |        | SI    |
| 5    | 5    | 005  |        | ENQ   | 16   | 10   | 020  |        | DLE   |
| 6    | 6    | 006  |        | ACK   | 17   | 11   | 021  |        | DC1   |
| 7    | 7    | 007  |        | BEL   | 18   | 12   | 022  |        | DC2   |
| 8    | 8    | 010  |        | BS    | 19   | 13   | 023  |        | DC3   |
| 9    | 9    | 011  |        | TAB   | 20   | 14   | 024  |        | DC4   |
| 10   | A    | 012  |        | LF    |

| Dec  | Hex  | Oct  | Html   | Char  | Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- | :--- | :--- | :--- | :----- | :---- |
| 21   | 15   | 025  |        | NAK   | 31   | 1F   | 037  |        | US    |
| 22   | 16   | 026  |        | SYN   | 32   | 20   | 040  | &#32;  | Space |
| 23   | 17   | 027  |        | ETB   | 33   | 21   | 041  | &#33;  | !     |
| 24   | 18   | 030  |        | CAN   | 34   | 22   | 042  | &#34;  | \"    |
| 25   | 19   | 031  |        | EM    | 35   | 23   | 043  | &#35;  | #     |
| 26   | 1A   | 032  |        | SUB   | 36   | 24   | 044  | &#36;  | $     |
| 27   | 1B   | 033  |        | ESC   | 37   | 25   | 045  | &#37;  | %     |
| 28   | 1C   | 034  |        | FS    | 38   | 26   | 046  | &#38;  | &     |
| 29   | 1D   | 035  |        | GS    | 39   | 27   | 047  | &#39;  | '     |
| 30   | 1E   | 036  |        | RS    | 40   | 28   | 050  | &#40;  | (     |

| Dec  | Hex  | Oct  | Html   | Char  | Dec  | Hex  | Oct  | Html  | Char |
| :--- | :--- | :--- | :----- | :---- | :--- | :--- | :--- | :---- | :--- |
| 41   | 29   | 051  | &#41;  | )     | 51   | 33   | 063  | &#51; | 3    |
| 42   | 2A   | 052  | &#42;  | *     | 52   | 34   | 064  | &#52; | 4    |
| 43   | 2B   | 053  | &#43;  | +     | 53   | 35   | 065  | &#53; | 5    |
| 44   | 2C   | 054  | &#44;  | ,     | 54   | 36   | 066  | &#54; | 6    |
| 45   | 2D   | 055  | &#45;  | -     | 55   | 37   | 067  | &#55; | 7    |
| 46   | 2E   | 056  | &#46;  | .     | 56   | 38   | 070  | &#56; | 8    |
| 47   | 2F   | 057  | &#47;  | /     | 57   | 39   | 071  | &#57; | 9    |
| 48   | 30   | 060  | &#48;  | 0     | 58   | 3A   | 072  | &#58; | :    |
| 49   | 31   | 061  | &#49;  | 1     | 59   | 3B   | 073  | &#59; | ;    |
| 50   | 32   | 062  | &#50;  | 2     | 60   | 3C   | 074  | &#60; | <    |

<!--
| Dec  | Hex  | Oct  | Html   | Char  || Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- || :--- | :--- | :--- | :----- | :---- |
| 61   | 3D   | 075  | &#61;  | =     |
| 62   | 3E   | 076  | &#62;  | >     |
| 63   | 3F   | 077  | &#63;  | ?     |
| 64   | 40   | 100  | &#64;  | @     |
| 65   | 41   | 101  | &#65;  | A     |
| 66   | 42   | 102  | &#66;  | B     |
| 67   | 43   | 103  | &#67;  | C     |
| 68   | 44   | 104  | &#68;  | D     |
| 69   | 45   | 105  | &#69;  | E     |
| 70   | 46   | 106  | &#70;  | F     |


| 71   | 47   | 107  | &#71;  | G     |
| 72   | 48   | 110  | &#72;  | H     |
| 73   | 49   | 111  | &#73;  | I     |
| 74   | 4A   | 112  | &#74;  | J     |
| 75   | 4B   | 113  | &#75;  | K     |
| 76   | 4C   | 114  | &#76;  | L     |
| 77   | 4D   | 115  | &#77;  | M     |
| 78   | 4E   | 116  | &#78;  | N     |
| 79   | 4F   | 117  | &#79;  | O     |
| 80   | 50   | 120  | &#80;  | P     |

| Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- |
| 81   | 51   | 121  | &#81;  | Q     |
| 82   | 52   | 122  | &#82;  | R     |
| 83   | 53   | 123  | &#83;  | S     |
| 84   | 54   | 124  | &#84;  | T     |
| 85   | 55   | 125  | &#85;  | U     |
| 86   | 56   | 126  | &#86;  | V     |
| 87   | 57   | 127  | &#87;  | W     |
| 88   | 58   | 130  | &#88;  | X     |
| 89   | 59   | 131  | &#89;  | Y     |
| 90   | 5A   | 132  | &#90;  | Z     |

| Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- |
| 91   | 5B   | 133  | &#91;  | [     |
| 92   | 5C   | 134  | &#92;  | \     |
| 93   | 5D   | 135  | &#93;  | ]     |
| 94   | 5E   | 136  | &#94;  | ^     |
| 95   | 5F   | 137  | &#95;  | _     |
| 96   | 60   | 140  | &#96;  | `     |
| 97   | 61   | 141  | &#97;  | a     |
| 98   | 62   | 142  | &#98;  | b     |
| 99   | 63   | 143  | &#99;  | c     |
| 100  | 64   | 144  | &#100; | d     |

| Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- |
| 101  | 65   | 145  | &#101; | e     |
| 102  | 66   | 146  | &#102; | f     |
| 103  | 67   | 147  | &#103; | g     |
| 104  | 68   | 150  | &#104; | h     |
| 105  | 69   | 151  | &#105; | i     |
| 106  | 6A   | 152  | &#106; | j     |
| 107  | 6B   | 153  | &#107; | k     |
| 108  | 6C   | 154  | &#108; | l     |
| 109  | 6D   | 155  | &#109; | m     |
| 110  | 6E   | 156  | &#110; | n     |

| Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- |
| 111  | 6F   | 157  | &#111; | o     |
| 112  | 70   | 160  | &#112; | p     |
| 113  | 71   | 161  | &#113; | q     |
| 114  | 72   | 162  | &#114; | r     |
| 115  | 73   | 163  | &#115; | s     |
| 116  | 74   | 164  | &#116; | t     |
| 117  | 75   | 165  | &#117; | u     |
| 118  | 76   | 166  | &#118; | v     |
| 119  | 77   | 167  | &#119; | w     |
| 120  | 78   | 170  | &#120; | x     |

| Dec  | Hex  | Oct  | Html   | Char  |
| :--- | :--- | :--- | :----- | :---- |
| 121  | 79   | 171  | &#121; | y     |
| 122  | 7A   | 172  | &#122; | z     |
| 123  | 7B   | 173  | &#123; | {     |
| 124  | 7C   | 174  | &#124; | \|    |
| 125  | 7D   | 175  | &#125; | }     |
| 126  | 7E   | 176  | &#126; | ~     |
| 127  | 7F   | 177  | &#127; | DEL   |
-->

---

## 2. Data Types In C

Reference: https://www.geeksforgeeks.org/data-types-in-c/

### 1. Integer Types

| Data Type              | Memory (bytes) | Range                           | Format Specifier |
| :--------------------- | :------------: | :------------------------------ | :--------------- |
| short int              |       2        | -32,768 to 32,767               | %hd              |
| unsigned short int     |       2        | 0 to 65,535                     | %hu              |
| unsigned int           |       4        | 0 to 4,294,967,295              | %u               |
| int                    |       4        | -2,147,483,648 to 2,147,483,647 | %d               |
| long int               |       4        | -2,147,483,648 to 2,147,483,647 | %ld              |
| unsigned long int      |       4        | 0 to 4,294,967,295              | %lu              |
| long long int          |       8        | -(2^63) to (2^63)-1             | %lld             |
| unsigned long long int |       8        | 0 to 18,446,744,073,709,551,615 | %llu             |


### 2. Floting Point Number

| Data Type   | Memory (bytes) | Range | Format Specifier |
| :---------- | :------------: | :---- | :--------------: |
| float       |       4        |       |        %f        |
| double      |       8        |       |       %lf        |
| long double |       16       |       |       %Lf        |

### 3. Character Types

| Data Type              | Memory (bytes) | Range                           | Format Specifier |
| :--------------------- | :------------- | :------------------------------ | :--------------- |
| signed char            | 1              | -128 to 127                     | %c               |
| unsigned char          | 1              | 0 to 255                        | %c               |

## 3. Operator

[sizeof operator](https://www.geeksforgeeks.org/sizeof-operator-c/)

| Operator Type         | Operator                                                     |
| :-------------------- | :----------------------------------------------------------- |
| Arithmetic operator   | +  ,   -   ,    *    ,    /    ,    %                        |
| Assignment operator   | =   ,   +=    ,  -=   ,  *=   ,   /=  ,   %=                 |
| Relational Operator   | >   ,  <   ,  ==  ,  !=  ,  >=  ,  <=                        |
| Logical Operator      | &&   ,  \|\|  ,   !                                          |
| Dereference operator  | int *p, q;  p = &q; *p = 100; // here * is Dereference operator |
| Two Pointer operators | *   ,   &                                                    |

