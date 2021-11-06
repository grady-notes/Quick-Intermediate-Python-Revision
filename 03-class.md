# Class

Class is an abstraction of a collection of objects. The class is also a blueprint for the objects. The entities of a class have common properties and methods.

An example of class Car is shown below:

```python
class Car:
    def __init__(self, _name, _color, _speed):
        self.name = _name
        self.color = _color
        self.speed = _speed
    def get_info(self):
        return (
            "Car name: "
            + self.name
            + "\n"
            + "Car Color: "
            + self.color
            + "\n"
            + "Car Speed: "
            + self.speed
        )
c = Car("Ferrari", "Red", "100km/h")
print(c.get_info())
```
