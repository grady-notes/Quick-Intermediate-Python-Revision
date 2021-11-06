# Generators

Generators in python are used to create iterators. Generators can be created using the `yield` keyword. The `yield` keyword is used to return a value from a function. This is similar to the return keyword, but the return keyword returns the value of the function, while the yield keyword returns a generator. Also that the return keyword will destroy each and every code inside the function, while the yield keyword will preserve the code inside the function so that it can be iterated over later.

An example of the yield keyword in combination with the for loop is shown below :

```python
def foo() :
    def next_car(arr) :
        for i in range(len(arr)) :
            yield arr[i]

    cars = ["Ford", "Volvo", "BMW"]
    iteration = next_car(cars)
    for i in range(len(cars)) :
        print(next(iteration))

foo()
```
