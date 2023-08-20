# Python Assignments

## Introduction

Each section describe an assignment which may be related to the ones that before it.
You need to use python 3.11 (latest stable release on Augest 2023). Type annotations are required.

## 2D Vector

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

### Bonus Point

- As you already know, we need to check type in operators' methods (like `__add__`). Read about `match` keyword in python and then implement that part 
  using `match` instead of `if-else`

## List of 2DVectors

After defing the 2DVector class, consider you have a list of these 2DVectors as follows:

```python
vectors: list[2DVector] = []
```

and you need to select the ones that have lentgh less than 2, using `filter` function in the python standard library.

## ND Vector

For the next step, we are going to create N-dimensional vector which is the parent
of our `2DVector`.
