# Functions

```
def hello():
    print('Howdy!')
    print('Howdy!!!')
    print('Hello there.')
```

### Arguments

- Most arguments are identified by their position in the function call.
- *keyword arguments* are identified by the keyword put before them in the function call.
    - `print('Hello', end='')`


### Return value

- The `return` statement uses the return keyword and value or expression that should be returned
- Numerous returns could be in a function to allow it to break early with a value
- Functions which do not return a value like print() still return the value 'None'
    - Behind the scenes, Python adds return None to the end of any func-tion definition with no return statement.

    
    
