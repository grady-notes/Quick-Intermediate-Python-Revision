# Iteration

Iteration is the process of repeating a process until a condition is met. In a loop, the condition is checked at the beginning of each iteration. Also, the process of going through each and every step of the loop is called an iteration. We can implement this iteration by using the iter function.

The iter function is used to create an iterator object. The iterator object is used to get the next value in the sequence.

An example of the iter function in combination with a basic for loop is shown below :

```python
def foo() :
    arr = ['hey', 'this', 'is', 'a', 'list']
    iteration = iter(arr)
    print("index, \tvalue")
    for i in range(len(arr)) :
        print(i, "\t", next(iteration))

foo()
```

The output will look like the following :

<table>
  <tr>
    <th>index</th>
    <th>value</th>
  </tr>
  <tr>
    <td>0</td>
    <td>hey</td>
  </tr>
  <tr>
    <td>1</td>
    <td>this</td>
  </tr>
  <tr>
    <td>2</td>
    <td>is</td>
  </tr>
  <tr>
    <td>3</td>
    <td>a</td>
  </tr>
  <tr>
    <td>4</td>
    <td>list</td>
  </tr>
</table>

The first column shows the index of the value in the list. The second column shows the value.

Similar to this forward iteration, we can also implement backward iteration using the reversed function.

An example of the reversed function in combination with a basic for loop is shown below :

```python
def foo() :
    arr = ['list', 'a', 'is', 'this', 'hey']
    iteration = reversed(arr)
    print("index, \tvalue")
    for i in range(len(arr)) :
        print(i, "\t", next(iteration))

foo()
```

The output will look like the following :

<table>
  <tr>
    <th>index</th>
    <th>value</th>
  </tr>
  <tr>
    <td>0</td>
    <td>hey</td>
  </tr>
  <tr>
    <td>1</td>
    <td>this</td>
  </tr>
  <tr>
    <td>2</td>
    <td>is</td>
  </tr>
  <tr>
    <td>3</td>
    <td>a</td>
  </tr>
  <tr>
    <td>4</td>
    <td>list</td>
  </tr>
</table>

Note that in the arr variable we have populated the list in reverse order. But in the output, the list is displayed in the same order as it was in the previous example. This is because the reversed function iterated the array backwards.

We can also create our own implementation of the iteration by creating a class and implementing the `__iter__` and `__next__` methods.

An example of the `__iter__` and `__next__` methods in combination with a basic for loop is shown below :

```python
def foo() :
    class Remote:
        def __init__(self, channels = []):
            self.channels = channels
            self.index = -1
        def __iter__ (self):
            return self
        def __next__ (self):
            self.index += 1
            if self.index == len(self.channels):
                raise StopIteration
            return self.channels[self.index]

    channels = ['BBC', 'CNN', 'FOX', 'ABC']
    remote = Remote(channels)
    iteration = iter(remote)
    for i in range(len(channels)) :
        print(next(iteration))

foo()
```
