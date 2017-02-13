# Lists

- Lists are a type of object used to store an indexed list of items
  - Can contain different types
  - Can be nested in other lists to create multidimensional arrays

`words = ['hello', 'world', '!']`

`print([words[0])`

### Create empty list

`empty_list = []`

### List operations

- Item at an index can be reassigned
- Lists can be added and mutiplied like strings
- Use the `in` operator to determine if an item is in the list
- Use `not in` operator to make sure item is not in list

### List functions

- Append to a list
  - `list.append(item)`
- Get number of items in a list
  - `len(list)`
- Insert an item into a list
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
  
  
