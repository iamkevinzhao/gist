## Projective Geometry and Transformations

- [Upper Level](README.md)

#### Projective Geometry and Transformations of 2D

Refer to Part 0: Chapter 2 of *Multiple View Geometry in Computer Vision*, Second Edition, by Richard Hartley.

**Homogeneous Representation of Lines**

**l**=(a, b, c)<sup>T</sup>, for ax+by+c=0.

**Homogeneous Representation of Points**

**x**=(x, y, 1)<sup>T</sup>

**Result 2.1.**

The point **x** lies on the line **l** if and only if **x**<sup>T</sup>**l**=0.

**Result 2.2.**

The intersection of two lines **l** and **l'** is the point **x**=**l**×**l'**.

**Example**

**l**=(-1, 0, 1)<sup>T</sup> , **l'**=(0, -1, 1), **x**=

```
|  i  j  k |   [1]
| -1  0  1 | = [1]
|  0 -1  1 |   [1]

Refer to Page 27.
```

**Result 2.4.**

The line through two points **x** and **x'** is **l**=**x**×**x'**.

