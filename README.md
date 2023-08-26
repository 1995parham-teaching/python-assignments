# Python Assignments

## Introduction

Each section describe an assignment which may be related to the ones that before it.
You need to use python 3.11 (latest stable release on August 2023). Type annotations are required.

## Basics

### 2D Vector

We want to design a new type in Python for handling 2D Vectors as follows:

```python
class Vector2d:
  def __init__(self, x: float, y: float):
    self.x = x
    self.y = y
```

We need to do the following operations on it:

```python
Vector2d(x1, y1) + Vector2d(x2, y2) == Vector2d(x1 + x2, y1 + y2)
Vector2d(x1, y1) + 1 raise ValueError()
Vector2d(x1, y1) * Vector2d(x2, y2) == Vector2d(x1 * x2, y1 * y2)
len(Vector2d(x1, y1)) == 2
Vector2d(x1, y1) @ Vector2d(x2, y2) == x1x2 + y1y2
Vector2d(x1, y1) - Vector2d(x2, y2) == Vector2d(x1 - x2, y1 - y2)
Vector2d(x1, y1) / Vector2d(x2, y2) raise ValueError()
```

We need to have a property for getting the vector length, and it should not be writable (we only can read it).

#### Bonus Point

- As you already know, we need to check type in operators' methods (like `__add__`). Read about `match` keyword in python and then implement that part
  using `match` instead of `if-else`

### List of `Vector2d`

After defining the `Vector2d` class, consider you have a list of these `Vector2d` as follows:

```python
vectors: list[Vector2d] = []
```

And you need to select the ones that have length less than 2, using `filter` function in the python standard library.

### ND Vector

For the next step, we are going to create N-dimensional vector which is the parent
of our `Vector2d`.

## Packages

### Remote calculator

Design a calculator that can handle users operations which includes:

- `add`: which adds two numbers and returns the result
- `sub`: which subtracts two numbers and returns the result
- `mul`: which multiplies two numbers and returns the result
- `div`: which divides two numbers and returns the result

Each operation has two operands which has the following format:

```
<operator> <op1> <op2>
add 1 2
sub 1 2
mul 10 2
```

and then for each operation you return a result in a single line:

```
<res>
3
-1
20
```

At end user close the connection with `exit`.

**You must handle multiple connections at the same time**.
