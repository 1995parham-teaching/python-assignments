# Python Assignments

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
```

We need to have a property for getting the vector length, and it should not be writable (we only can read it).

## ND Vector

For the next step, we are going to create N-dimensional vector which is the parent
of our `2DVector`.
