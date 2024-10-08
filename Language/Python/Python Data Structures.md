# List
List is an ordered, variable-length collection that allows you to store a mix of different data types.

**Example**
```python
my_list = [1, 2, 3, "apple", [5, 6]] print(my_list[0]) 
my_list[1] = "banana" 
```
# List related function
- `list.append()`: Add element at the end of the list. 
- `list.extend()`: Add list or iterable object at the end of the list. 
- `list.insert(index, item)`: Add item in index
- `list.remove(item)`: Remove certain elements that appear first from the list.
- `list.pop(index)`: Remove an element in a specific location from the list and return the element. If you do not specify an index, remove the last element and return it.
- `list.clear()`: Remove all of list's element.
- `list.sort(key=None, reverse=False)`: Sort elements in the list in ascending order. If reverse=True is set, it is sorted in descending order. You can also apply custom sorting criteria using the key.
# Tuple
Tuple is data structure that similar **list** but immutable. Because tuple can't add or remove element, it is useful for save data that don't have to change. The tuple is created using brackets `()`. However, if there is only one element, it must be followed by a comma`(,)`.

**Example**
```python
my_tuple = (1, 2, 3)
print(my_tuple)  # print: (1, 2, 3)

single_element_tuple = (1,)
print(single_element_tuple)  # print: (1,)
```
# Tuple related function
Because tuple cannot change, mostly functions provide inquiry or conversion functions.
- `tuple.count()`: Returns how many times a particular element appears in a tuple.
- `tuple.index()`: Returns the first index of a particular element in the tuple.
- `in` operator: Verify that the tuple contains certain elements.
- `+` operator: Connect two tuples to create a new tuple.
- `*` operator: Repeat the elements of the tuple to create a new tuple.
- `tuple()`: Translate other repeatable objects (lists, strings, etc.) into tuples.
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
