# Strings

- A strings is essentially a "list" of characters and can do many of the same interactions
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

