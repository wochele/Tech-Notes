# Exception handling

Errors can be handled with try and except statements. The code that could potentially have an error is put in a try clause. The program execu-tion moves to the start of a following except clause if an error happens.

```
def spam(divideBy):
    try:
        return 42 / divideBy
    except ZeroDivisionError:
        print('Error: Invalid argument.')
```

When code in a try clause causes an error, the program execution immediately moves to the code in the except clause. After running that code, the execution continues as normal.

The execution does not return into the try clause where the error occurred.
