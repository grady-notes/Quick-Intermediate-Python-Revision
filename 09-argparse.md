# Command Line Argparse

Passing arguments to your program is as easy as typing them on the command line. This is considered the most common way to pass arguments to your program. This is also a very basic skill for a programmer. We can use the argparse module to make this a lot easier.

An argparse module is a Python module that allows you to parse command line arguments.

An example of how to use argparse is shown below :

```python
import argparse

def foo() :
    parser = argparse.ArgumentParser()
    args = parser.parse_args()

foo()
```

Execute the above code with the command `python main.py -h` to see the help message. This is the same as typing `python main.py --help`. The -h argument is the default argument that is provided by the argparse module. However, you can provide your own arguments.

An example of how to add arguments to the argparse module is shown below :

```python
import argparse

def foo() :
    parser = argparse.ArgumentParser()
    parser.add_argument('arg', help='This is the first argument.')
    args = parser.parse_args()
    def print_args() :
        return args.arg
    print('Your Arg : ', print_args())

foo()
```

This can be executed by `python main.py any_argument_here`.

To make an argument optional, you can use the `--` argument.

An example of how to make an argument optional is shown below :

```python
import argparse

def foo() :
    parser = argparse.ArgumentParser()
    parser.add_argument('--arg', help='This is the optional argument.')
    args = parser.parse_args()
    def print_args() :
        return args.arg
    print('Your Arg : ', print_args())

foo()
```

This can be executed by `python main.py --arg any_argument_here`.
