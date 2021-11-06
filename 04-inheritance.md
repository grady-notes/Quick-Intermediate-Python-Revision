# Inheritance

Deriving subclasses from a base class is a common way to implement inheritance. In order to derive a class from a base class, you must define a new class that derives from the base class by passing the base class as the first argument to the class definition.

An example of inheriting from a base class is shown below:

```python
def foo() :
    class Vehicle:
    def general_use(self):
        print("Used for transport")

    class Car(Vehicle):
        def info(self):
            print("Has 4 wheels")
    class Bike(Vehicle):
        def info(self):
            print("Has 2 wheels")

    car = Car()
    car.info()
    car.general_use()

    bike = Bike()
    bike.info()
    bike.general_use()

foo()
```

Just like in C++ and other programming languages, the base class is defined before the derived class. Similar to this inheritance we have one more similar topic known as multiple inheritance.

Multiple inheritance is a way to inherit from more than one base class. In order to inherit from more than one base class, you must define a new class that derives from all the base classes by passing the base classes as the first arguments to the class definition.

An example of multiple inheritance is shown below:

```python
def foo() :
    class Father:
        def books(self):
            print("I like to read books")
    class Mother:
        def cakes(self):
            print("I like to bake cakes")

    class Child(Father, Mother):
        def hobby(self):
            print("I like to play video games")

    child = Child()
    c.books()
    c.cakes()
    c.hobby()

foo()
```
