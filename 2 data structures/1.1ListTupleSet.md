## Differences Between Lists, Tuples, and Sets

### 1. **Lists**:
- **Definition**: A list is an ordered and mutable collection of items, which means you can change, add, or remove elements after the list is created.
- **Syntax**: Lists are defined using square brackets `[]`.
- **Allow Duplicates**
- **Indexed**: lists are indexed, meaning you can access elements using their position.
  
##### Example:
```python
my_list = [1, 2, 3, 4, 5]
print(my_list)        # Output: [1, 2, 3, 4, 5]

# Accessing elements
print(my_list[0])     # Output: 1

# Modifying elements
my_list[2] = 10
print(my_list)        # Output: [1, 2, 10, 4, 5]

# Adding elements
my_list.append(6)
print(my_list)        # Output: [1, 2, 10, 4, 5, 6]

# Removing elements
my_list.remove(10)
print(my_list)        # Output: [1, 2, 4, 5, 6]
```

### 2. **Tuples**:
- **Definition**: A tuple is an ordered and immutable collection of items, which means once a tuple is created, you cannot change its elements.
- **Syntax**: Tuples are defined using parentheses `()`.
- **Allow Duplicates**
- **Indexed**: tuples are indexed, meaning you can access elements using their position.

##### Example:
```python
# Creating a tuple
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple)  # Output: (1, 2, 3, 4, 5)

# Accessing elements using indexing
print(my_tuple[0])  # Output: 1

# Trying to modify a tuple (This will raise an error)
# my_tuple[1] = 10  # TypeError: 'tuple' object does not support item assignment

# Concatenating tuples
new_tuple = my_tuple + (6, 7)
print(new_tuple)  # Output: (1, 2, 3, 4, 5, 6, 7)

# Nested tuple
nested_tuple = (1, 2, (3, 4), 5)
print(nested_tuple)  # Output: (1, 2, (3, 4), 5)

# Tuple with single element (Note the comma)
single_element_tuple = (10,)
print(single_element_tuple)  # Output: (10,)

# Unpacking tuple
a, b, c, d, e = my_tuple

```

### 3. **Sets**:
- **Definition**: A set is an unordered and mutable collection of unique elements. This means it does not allow duplicate elements and does not maintain any specific order.
- **Syntax**: Sets are defined using curly braces `{}` or the `set()` function.
- **No Duplicates**: sets only allow unique elements.
- **No Indexed**: sets do not support indexing because they are unordered.

##### Example Usage of Set
```python
# Creating a set
my_set = {1, 2, 3, 4, 5}
print(my_set)  # Output: {1, 2, 3, 4, 5}

# Adding elements to a set
my_set.add(6)
print(my_set)  # Output: {1, 2, 3, 4, 5, 6}

# Removing elements from a set
my_set.remove(3)
print(my_set)  # Output: {1, 2, 4, 5, 6}

# Sets do not allow duplicate elements
my_set.add(2)
print(my_set)  # Output: {1, 2, 4, 5, 6} (no duplicate 2)

# Set operations: Union, Intersection, Difference
set_a = {1, 2, 3}
set_b = {3, 4, 5}

# Union
print(set_a | set_b)  # Output: {1, 2, 3, 4, 5}

# Intersection
print(set_a & set_b)  # Output: {3}

# Difference
print(set_a - set_b)  # Output: {1, 2}

```

### Summary Table:

| Feature             | **List**                          | **Tuple**                        | **Set**                            |
|---------------------|-----------------------------------|----------------------------------|------------------------------------|
| **Ordered**         | Yes                               | Yes                              | No                                 |
| **Mutable**         | Yes                               | No (immutable)                   | Yes (mutable)                      |
| **Duplicates**      | Yes                               | Yes                              | No (unique elements only)          |
| **Indexed**         | Yes (supports indexing)           | Yes (supports indexing)          | No (no indexing)                   |
| **Syntax**          | `[]`                              | `()`                             | `{}`                               |
| **Use Case**        | General-purpose, flexible storage | Fixed collections, return values | Unordered collections, set operations like union, intersection, difference |
| **Methods**         | Many built-in methods like `append()`, `remove()` | Fewer built-in methods due to immutability | Methods like `add()`, `remove()`, set operations |
| **Performance**     | Slower than tuples due to mutability | Faster than lists because of immutability | Faster membership tests, but unordered |
| **Immutability**    | No (elements can be changed)      | Yes (elements cannot be changed) | No (but elements themselves must be immutable) |
