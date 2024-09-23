# Dictionary
In Python, a dictionary is a type of data that stores data as a pair of key-value. The dictionary declares itself as a brace `{}`, each key and value separated by a colon`:`, and multiple key-value pairs separated by commas, . The key must be unique and can only be of non-changeable datatypes (`string`, `number`, `tuple`, etc.). On the other hand, the value can be of any datatype and can be duplicated.

**Example**
```python
# dictionary define
student = {
    "name": "John",  # key: 'name', value: 'John'
    "age": 20,       # key: 'age', value: 20
    "major": "DevOps"  # key: 'major', value: 'DevOps'
}

print(student["name"])  # print: John
print(student["age"])   # print: 20
```
# Dictionary related function
- `dict.get(key[, default])`: Returns a value corresponding to the key, and if the key is not present, returns a value of 'default'.
- `dict.keys()`: Returns dictionary's all of keys.
- `dict.values()`: Returns dictionary's all of values.
- `dict.items()`: Returns dictionary's key-value pair as tuple.
- `dict.update(dict2)`: Add or update the key-value pair of other dictionaries to the current dictionary.
- `dict.pop(key[, default])`: Delete a specific key and return its value. If the key is not present, return the value 'default'.
# Dictionary Loop
```python
for key, value in student.items(): # first variable is key, second variable is value
    print(key, value)
```

---
Reference link 🙂   
https://docs.python.org/3/tutorial/datastructures.html
