# Working with JSON in Python

JSON (JavaScript Object Notation) is a lightweight data-interchange format standardized by the ECMAScript team. It is similar to XML, but is designed to be easy for humans to read and write.

JSON objects can be created in python using the json module that comes built in with the python interpreter.

An example would be,

```python
import json
def makeObj() :
    obj = {}
    obj['aatif'] = {
        'name': 'Aatif',
        'age': 19
    }
    obj['grady'] = {
        'name': 'Grady',
        'age': 20
    }
    final = json.dumps(obj)
    return final
print(makeObj())
```

This will create an object in the JSON format, and return it as a string.

Now that we know how to create an object in python, let us save that into a separate JSON file.

```python
import json
def makeObj() :
    obj = {}
    obj['aatif'] = {
        'name': 'Aatif',
        'age': 19
    }
    obj['grady'] = {
        'name': 'Grady',
        'age': 20
    }
    final = json.dumps(obj)
    return final
with open('data.json', 'w') as f:
    f.write(makeObj())
```

This will create a file called data.json in the current directory and write the JSON object to it. The file can be opened and read as follows.

```python
import json

with open('data.json', 'r') as f:
    data = json.load(f)
    print(data)
```
