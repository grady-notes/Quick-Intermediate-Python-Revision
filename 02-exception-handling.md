# Exception Handling

Exceptions are the abnormalities that occur during the execution of a program. Exception handling is the process of handling such abnormalities.

This can be done using the try-except block.

```python
def foo() :
    x = 1
    y = 0
    try :
        z = x/y
    except Exception as e :
        print(e)
```

This will throw a ZeroDivisionError since we are trying to divide a number by zero. But now the program will not terminate abnormally, instead it will continue to execute the rest of the code and exit normally.
