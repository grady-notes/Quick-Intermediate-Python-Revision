# Raise Exceptions

Exceptions are used to signal that something went wrong. These exceptions can be raised by the programmer or by the interpreter. To do so we use the keyword `raise`.

An example of a raise exception is shown below:

```python
def foo() :
    try :
        raise MemoryError("Out of memory")
    except Exception as e :
        print(e)

foo()
```

This code will raise a memory error execption saying `Out of memory`. But this is just for the built in exceptions. We can also raise our own exceptions by creating a derived class from the `Exception` class.

An example of creating an exception is shown below:

```python
def foo() :
    class Error (Exception) :
        def __init__(self, message) :
            self.message = message
        def print(self) :
            print("Error : " + str(self.message))

    try :
        raise Error("Out of memory")
    except Exception as e :
        print(e)

foo()
```
