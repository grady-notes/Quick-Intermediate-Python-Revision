# Comprehensions

Comprehensions are a way to create lists from other lists. The same syntax works for list, set, and dictionaries.

In this array of numbers, `arr = [1,2,3,4]`, we can create a new list of numbers that are the square of the numbers in the original list. To do this we would have to run a for loop which would go through each number in the original list, square it, and add it to a new list. This would be a lot of work to do resulting in inefficient code. Hence, we can use a comprehension to create a new list of the squares of the numbers in the original list.

An example of a list comprehension is shown below :

```python
arr = [1,2,3,4]
squares = [num**2 for num in arr]
print(squares)
```

An example of a set comprehension is shown below :

```python
s = set([1,2,3,4])
squares = {num**2 for num in s}
print(squares)
```

Dictionaries can be created using a comprehension as well. This would require 2 different lists to be zipped together using the `zip` function.

An example of a dictionary comprehension is shown below :

```python
def foo() :
    cities = ['New York', 'London', 'Paris', 'Berlin']
    countries = ['USA', 'UK', 'France', 'Germany']
    zipped = zip(cities, countries)
    dictionary = {city: country for city, country in zipped}
    print(dictionary)

foo()
```
