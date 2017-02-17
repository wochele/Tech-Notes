# Strings

- A strings is essentially a "list" of characters and can do many of the same interactions
- Strings use indexes and slices the same way lists do
- The `in` and `not in` operators can be used with strings just like with list values.
- Strings are *immutable*
  - The proper way to “mutate” a string is to use slicing and concatenation to build a new string by copying from parts of the old string.
  
### Raw strings

You can place an r before the beginning quotation mark of a string to make it a raw string. A raw string completely ignores all escape characters and prints any backslash that appears in the string. 

```
>>> print(r'That is Carol\'s cat.')
That is Carol\'s cat.
```
### Multiline strings with triple-quotes

A multiline string in Python begins and ends with either three single quotes or three double quotes. Any quotes, tabs, or newlines in between the “triple quotes” are considered part of the string. Python’s indentation rules for blocks do not apply to lines inside a multiline string.

### String methods

- The `upper()` and `lower()` string methods return a new string where all the letters in the original string have been converted to uppercase or lower-case,respectively.

```
>>>spam = 'Hello world!'
>>> spam = spam.upper()
>>> spam
'HELLO WORLD!'

>>> spam = spam.lower()
>>> spam
'hello world!'
```

- The isupper() and islower() methods will return a Boolean True value if the string has at least one letter and all the letters are uppercase or lowercase, respectively. Otherwise, the method returns False

