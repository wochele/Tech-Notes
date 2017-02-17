# Dictionary data type

- Collection of many values
- Indexes for dictionaries can use many different data types, not just integers.
- Indexes for dictionaries are called keys, and a key with its associ-ated value is called a key-value pair.
- Items in dictionaries are unordered.
- Use `in` to see if a key is in the list

```
myCat = {'size': 'fat', 'color': 'gray', 'disposition': 'loud'}
```

There are three dictionary methods that will return list-like values of the dictionary’s keys, values, or both keys and values: keys(), values(), and items().

```
spam = {'color': 'red', 'age': 42}
for v in spam.values():
    print(v)
```

```
for k in spam.keys():
    print(k)
```

```
for i in spam.items():
    print(i)
```

```
spam = {'name': 'Zophie', 'age': 7}

'name' in spam.keys()
True

'Zophie' in spam.values()
True

'color' in spam.keys()
False

'color' not in spam.keys()
True

'color' in spam
False
```

It’s tedious to check whether a key exists in a dictionary before accessing that key’s value. Fortunately, dictionaries have a get() method that takes two arguments: the key of the value to retrieve and a fallback value to return if that key does not exist.

setdefault() method - The first argument passed to the method is the key to check for, and the second argument is the value to set at that key if the key does not exist. If the key does exist, the setdefault() method returns the key’s value. 

If you import the pprint module into your programs, you’ll have access to the pprint() and pformat() functions that will “pretty print” a dictionary’s values. This is helpful when you want a cleaner display of the items in a dictionary than what print() provides

