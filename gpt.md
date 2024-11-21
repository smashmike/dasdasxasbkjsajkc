

---

### **Sets**
- **Create**: `{1, 2, 3}`, `set()`
- **Add**: `my_set.add(4)`
- **Remove**: `my_set.remove(2)`, `my_set.discard(3)`, `my_set.pop()`, `my_set.clear()`
- **Check**: `1 in my_set`
- **Ops**:  
  - Union: `set1 | set2` or `.union()`
  - Intersection: `set1 & set2` or `.intersection()`
  - Difference: `set1 - set2` or `.difference()`
  - Symmetric Diff: `set1 ^ set2` or `.symmetric_difference()`
- **Methods**: `.update()`, `.intersection_update()`, `.difference_update()`, `.symmetric_difference_update()`
- **Comprehension**: `{x*x for x in range(5)}`
- **Frozen Sets**: `frozenset([1, 2, 3])`

---

### **Dictionaries**
- **Create**: `my_dict = {"key": "value"}`
- **Access**: `value = my_dict["key"]`, `my_dict.get("key", default)`
- **Add/Update**: `my_dict["key"] = "new_value"`
- **Remove**: `del my_dict["key"]`, `my_dict.pop("key")`
- **Check**: `"key" in my_dict`
- **Iterate**: 
  - `for k, v in my_dict.items():`
- **Methods**: `.keys()`, `.values()`, `.items()`, `.update()`, `.clear()`
- **Comprehension**: `{x: x*x for x in range(5)}`
- **Merge**: `dict1 | dict2` (Python 3.9+)
- **Nested Dicts**: `{ "outer": { "inner": "value" } }`

---

### **Classes**
- **Syntax**:
  ```python
  class MyClass:
      def __init__(self, attr): self.attr = attr
      def method(self): return self.attr
  ```
- **Inheritance**: `class Child(Parent):`
- **Override**: Redefine parent methods in the child.
- **Special Methods**:
  - `__str__`: Custom `str(obj)`
  - `__repr__`: Debug string
  - `__len__`: Custom `len(obj)`
- **Static/Class Methods**:
  ```python
  @staticmethod def static(): pass
  @classmethod def cls_method(cls): pass
  ```
- **Properties**:
  ```python
  @property def attr(self): return self._attr
  @attr.setter def attr(self, val): self._attr = val
  ```

---

### **Algorithms**
- **Linear Search**: O(n)  
  ```python
  def linear_search(arr, target):
      for i in arr: if i == target: return i
  ```
- **Binary Search**: O(log n) (sorted input)  
  ```python
  def binary_search(arr, t):
      l, r = 0, len(arr)-1
      while l <= r:
          m = (l+r)//2
          if arr[m] == t: return m
          elif arr[m] < t: l = m+1
          else: r = m-1
  ```
---

### **Sorting**
- **Insertion Sort**: O(n^2), stable  
  ```python
  def insertion_sort(arr):
      for i in range(1, len(arr)):
          key, j = arr[i], i-1
          while j >= 0 and arr[j] > key: arr[j+1], j = arr[j], j-1
          arr[j+1] = key
  ```
- **Merge Sort**: O(n log n), stable  
  ```python
  def merge_sort(arr):
      if len(arr) > 1:
          m = len(arr)//2; L, R = arr[:m], arr[m:]
          merge_sort(L); merge_sort(R)
          i=j=k=0
          while i < len(L) and j < len(R):
              if L[i] < R[j]: arr[k] = L[i]; i+=1
              else: arr[k] = R[j]; j+=1
              k+=1
          arr[k:] = L[i:] + R[j:]
  ```
- **Python Sort**: O(n log n), stable  
  - `list.sort()`: In-place  
  - `sorted()`: Returns new list  
  ```python
  sorted(arr, key=len, reverse=True)
  ```

---

### **Big O Complexity**
| Name               | Complexity | Example                      |
|--------------------|------------|------------------------------|
| Constant Time      | O(1)       | Accessing element by index   |
| Logarithmic Time   | O(log n)   | Binary search                |
| Linear Time        | O(n)       | Iterating a list             |
| Linearithmic Time  | O(n log n) | Merge sort                   |
| Quadratic Time     | O(n^2)     | Nested loops                 |
| Exponential Time   | O(2^n)     | Recursive fib                |

---

This format keeps the most essential details while fitting into a concise, exam-ready format.