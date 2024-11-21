
---

### **Sets**
- **Create**: `{1, 2, 3}`, `set()`
- **Add**: `my_set.add(4)`
- **Remove**:  
  - `my_set.remove(2)` (KeyError if missing)  
  - `my_set.discard(3)` (no error if missing)  
  - `my_set.pop()` (arbitrary)  
  - `my_set.clear()` (all elements)  
- **Check**: `1 in my_set`
- **Ops**:  
  - **Union**: `set1 | set2`, `.union(set2)`  
  - **Intersection**: `set1 & set2`, `.intersection(set2)`  
  - **Diff**: `set1 - set2`, `.difference(set2)`  
  - **Sym Diff**: `set1 ^ set2`, `.symmetric_difference(set2)`  
- **Methods**: `.update()`, `.intersection_update()`, `.difference_update()`, `.symmetric_difference_update()`  
- **Comp**: `{x*x for x in range(6)}`  
- **Frozen Set**: `frozenset([1, 2, 3])`  
- **Length**: `len(my_set)`
- **Copy**: `new_set = my_set.copy()`
- **Subset/Superset**:  
  - `set2.issubset(set1)`  
  - `set1.issuperset(set2)`  

---

### **Dictionaries**
- **Create**: `{"key": "value"}`  
- **Access**: `my_dict["key"]`, `my_dict.get("key", default)`  
- **Add/Update**: `my_dict["key"] = "value"`  
- **Remove**:  
  - `del my_dict["key"]`  
  - `my_dict.pop("key")` (returns value)  
- **Check**: `"key" in my_dict`
- **Iterate**:  
  ```python
  for k, v in my_dict.items(): print(k, v)
  ```
- **Methods**:  
  - `.keys()`, `.values()`, `.items()`  
  - `.update(other_dict)`, `.clear()`  
- **Comp**: `{x: x*x for x in range(6)}`  
- **Nested**: `{"outer": {"inner": "value"}}`  
- **Default Dict**:  
  ```python
  from collections import defaultdict
  dd = defaultdict(int)
  dd["key"] += 1
  ```
- **Merge**: `merged = dict1 | dict2`  
- **Copy**: `new_dict = my_dict.copy()`  

---

### **Classes**
- **Syntax**:  
  ```python
  class MyClass: pass
  obj = MyClass()
  ```
- **Init**:  
  ```python
  class MyClass:
      def __init__(self, attr): self.attr = attr
  ```
- **Instance Method**:  
  ```python
  def method(self): return self.attr
  ```
- **Attributes**:  
  - **Class**: Shared: `class_attr = "shared"`  
  - **Instance**: Unique: `self.attr = value`  
- **Inheritance**: `class Child(Parent):`  
  - **Override**: Redefine parent methods in child.
  - **Super()**: Access parent:  
    ```python
    super().__init__(parent_arg)
    ```
- **Private**: `_private_attr`, `_private_method()`
- **Special Methods**:  
  - `__str__`: User-friendly string  
  - `__repr__`: Debug string  
  - `__len__`: Custom `len(obj)`  
- **Class Method**: Modify shared state:  
  ```python
  @classmethod def cls_method(cls): cls.attr += 1
  ```
- **Static Method**: Utility:  
  ```python
  @staticmethod def utility(): pass
  ```
- **Properties**:  
  ```python
  @property def attr(self): return self._attr
  @attr.setter def attr(self, value): self._attr = value
  ```

---