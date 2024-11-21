# Sets

1. **Syntax**:
   ```python
   my_set = {1, 2, 3}
   empty_set = set()  # Note: {} creates an empty dictionary, not a set
   ```

3. **Adding Elements**:
   ```python
   my_set.add(4)
   ```

4. **Removing Elements**:
   ```python
   my_set.remove(2)  # Raises KeyError if the element is not found
   my_set.discard(3)  # Does not raise an error if the element is not found
   my_set.pop()  # Removes and returns an arbitrary element
   my_set.clear()  # Removes all elements
   ```

5. **Checking for Elements**:
   ```python
   if 1 in my_set:
       print("1 is in the set")
   ```

6. **Set Operations**:
   - **Union**:
     ```python
     set1 = {1, 2, 3}
     set2 = {3, 4, 5}
     union_set = set1 | set2  # {1, 2, 3, 4, 5}
     union_set = set1.union(set2)
     ```
   - **Intersection**:
     ```python
     intersection_set = set1 & set2  # {3}
     intersection_set = set1.intersection(set2)
     ```
   - **Difference**:
     ```python
     difference_set = set1 - set2  # {1, 2}
     difference_set = set1.difference(set2)
     ```
   - **Symmetric Difference**:
     ```python
     sym_diff_set = set1 ^ set2  # {1, 2, 4, 5}
     sym_diff_set = set1.symmetric_difference(set2)
     ```

7. **Set Methods**:
   - `my_set.update(other_set)`: Adds elements from `other_set` to `my_set`.
   - `my_set.intersection_update(other_set)`: Updates `my_set` with the intersection of `my_set` and `other_set`.
   - `my_set.difference_update(other_set)`: Updates `my_set` with the difference of `my_set` and `other_set`.
   - `my_set.symmetric_difference_update(other_set)`: Updates `my_set` with the symmetric difference of `my_set` and `other_set`.

8. **Set Comprehensions**:
   ```python
   squares = {x*x for x in range(6)}
   ```

9. **Frozen Sets**: Immutable sets.
   ```python
   frozen_set = frozenset([1, 2, 3])
   ```

10. **Length of a Set**:
    ```python
    length = len(my_set)
    ```

11. **Copying Sets**:
    ```python
    new_set = my_set.copy()
    ```

12. **Subset and Superset**:
    ```python
    set1 = {1, 2, 3}
    set2 = {1, 2}
    is_subset = set2.issubset(set1)  # True
    is_superset = set1.issuperset(set2)  # True
    ```

# Dictionaries

1. **Syntax**:
   ```python
   my_dict = {
       "key1": "value1",
       "key2": "value2",
       "key3": "value3"
   }
   ```

2. **Accessing Values**:
   ```python
   value = my_dict["key1"]
   ```

3. **Adding/Updating Items**:
   ```python
   my_dict["key4"] = "value4"  # Adds a new key-value pair
   my_dict["key1"] = "new_value1"  # Updates the value of an existing key
   ```

4. **Removing Items**:
   ```python
   del my_dict["key1"]  # Removes the key-value pair with key "key1"
   value = my_dict.pop("key2")  # Removes the key-value pair and returns the value
   ```

5. **Checking for Keys**:
   ```python
   if "key1" in my_dict:
       print("Key1 is present")
   ```

6. **Iterating Through a Dictionary**:
   ```python
   for key in my_dict:
       print(key, my_dict[key])
   
   for key, value in my_dict.items():
       print(key, value)
   ```

7. **Dictionary Methods**:
   - `my_dict.keys()`: Returns a view object of all keys.
   - `my_dict.values()`: Returns a view object of all values.
   - `my_dict.items()`: Returns a view object of all key-value pairs.
   - `my_dict.get("key", default)`: Returns the value for "key" if it exists, otherwise returns `default`.
   - `my_dict.clear()`: Removes all items from the dictionary.
   - `my_dict.update(other_dict)`: Updates the dictionary with key-value pairs from `other_dict`.

8. **Dictionary Comprehensions**:
   ```python
   squares = {x: x*x for x in range(6)}
   ```

9. **Nested Dictionaries**:
    ```python
    nested_dict = {
        "dict1": {"key1": "value1"},
        "dict2": {"key2": "value2"}
    }
    ```

10. **Default Dictionaries** (from `collections` module):
    ```python
    from collections import defaultdict
    dd = defaultdict(int)
    dd["key1"] += 1
    ```

11. **Ordered Dictionaries** (from `collections` module):
    ```python
    from collections import OrderedDict
    od = OrderedDict()
    od["key1"] = "value1"
    od["key2"] = "value2"
    ```

12. **Dictionary Views**:
    - `dict.keys()`: Returns a view object of the dictionary's keys.
    - `dict.values()`: Returns a view object of the dictionary's values.
    - `dict.items()`: Returns a view object of the dictionary's key-value pairs.

13. **Merging Dictionaries** (Python 3.9+):
    ```python
    dict1 = {"a": 1, "b": 2}
    dict2 = {"b": 3, "c": 4}
    merged_dict = dict1 | dict2  # {'a': 1, 'b': 3, 'c': 4}
    ```

14. **Dictionary Length**:
    ```python
    length = len(my_dict)
    ```

15. **Copying Dictionaries**:
    ```python
    new_dict = my_dict.copy()
    ```

# Classes

1. **Syntax**:
   ```python
   class MyClass:
       pass
   ```

3. **Creating an Instance**:
   ```python
   obj = MyClass()
   ```

4. **The `__init__` Method**: The constructor method for initializing an object's attributes.
   ```python
   class MyClass:
       def __init__(self, attribute1, attribute2):
           self.attribute1 = attribute1
           self.attribute2 = attribute2
   ```

5. **Instance Methods**: Functions defined within a class that operate on instances of the class.
   ```python
   class MyClass:
       def __init__(self, attribute):
           self.attribute = attribute

       def method(self):
           return self.attribute
   ```

6. **Class Attributes**: Attributes that are shared among all instances of the class.
   ```python
   class MyClass:
       class_attribute = "I am a class attribute"
   ```

7. **Instance Attributes**: Attributes that are unique to each instance.
   ```python
   class MyClass:
       def __init__(self, attribute):
           self.instance_attribute = attribute
   ```

8. **Inheritance**: A way to form new classes using classes that have already been defined.
   ```python
   class ParentClass:
       pass

   class ChildClass(ParentClass):
       pass
   ```

9. **Method Overriding**: Redefining a method in the child class that was defined in the parent class.
   ```python
   class ParentClass:
       def method(self):
           return "Parent"

   class ChildClass(ParentClass):
       def method(self):
           return "Child"
   ```

10. **The `super()` Function**: Used to call a method from the parent class.
    ```python
    class ParentClass:
        def __init__(self, attribute):
            self.attribute = attribute

    class ChildClass(ParentClass):
        def __init__(self, attribute, extra_attribute):
            super().__init__(attribute)
            self.extra_attribute = extra_attribute
    ```

11. **Private Attributes and Methods**: By convention, attributes and methods intended to be private are prefixed with an underscore.
    ```python
    class MyClass:
        def __init__(self, attribute):
            self._private_attribute = attribute

        def _private_method(self):
            pass
    ```

12. **Special Methods**: Also known as magic methods or dunder methods, they allow instances of the class to interact with Python's built-in functions and operators.
    - `__str__`: Defines the string representation of an object.
      ```python
      class MyClass:
          def __str__(self):
              return "String representation"
      ```
    - `__repr__`: Defines the official string representation of an object.
      ```python
      class MyClass:
          def __repr__(self):
              return "Official string representation"
      ```
    - `__len__`: Defines the behavior of the `len()` function.
      ```python
      class MyClass:
          def __len__(self):
              return 42
      ```

13. **Class Methods**: Methods that are bound to the class and not the instance. They can modify class state that applies across all instances of the class.
    ```python
    class MyClass:
        class_attribute = 0

        @classmethod
        def class_method(cls):
            cls.class_attribute += 1
    ```

14. **Static Methods**: Methods that do not modify class or instance state. They are utility functions.
    ```python
    class MyClass:
        @staticmethod
        def static_method():
            return "I am a static method"
    ```

15. **Properties**: A way of customizing access to instance attributes.
    ```python
    class MyClass:
        def __init__(self, attribute):
            self._attribute = attribute

        @property
        def attribute(self):
            return self._attribute

        @attribute.setter
        def attribute(self, value):
            self._attribute = value
    ```
