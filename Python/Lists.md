# Lists

- Lists are a type of object used to store an indexed list of items
  - Can contain different types
  - Can be nested in other lists to create multidimensional arrays
  - Accessed by their position in the list 0 based
  - Can assign values by using the position `list[1] = x`
  - When you assign a list to a variable, you are actually assigning a list reference to the variable.

`words = ['hello', 'world', '!']`

`print([words[0])`

### Create empty list

`empty_list = []`

### List operations

- Item at an index can be reassigned
- Lists can be added and mutiplied like strings
- Use the `in` operator to determine if an item is in the list
- Use `not in` operator to make sure item is not in list

### Negative Indexes

- Index [-1] refers to the last item in a list
- Index [-2] refers to the second to last item and so on

### List Slices

- list[1:4] retrieves list starting at 1 through but not including 4
- list[:4] is the same as list[0:4]

### List functions

- Append to a list
  - `list.append(item)`
- Remove value from a list
  - del list[1]
    - Removes the values and shift the other values
- Get number of items in a list
  - `len(list)`
- Insert an item into a list
  - list = list + [item]
  - `list.insert(index, item)`
- Find the first occurance of an item and return the index, if not raise ValueError
  - `list.index(item)`
- Return item with maximum value
  - max(list)
- Return item with minimum value
  - min(list)
- Return how many times an item appears in a list
  - list.count(item)
- Remove an item from a list
  - list.remove(item)
- Reverse the objects in a list
  - list.reverse()
- Sort items in a list
  - list.sort()
  
### Iterate over items in a list

```
for i in range(len(supplies)):
    print('Index ' + str(i) + ' in supplies is: ' + supplies[i])
```

### Multiple assignment trick

The following are equivalent

```
cat = ['fat', 'black', 'loud']
size = cat[0]
color = cat[1]
disposition = cat[2]
```

```
cat = ['fat', 'black', 'loud']
size, color, disposition = cat
```

