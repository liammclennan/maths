Vectors
====

[Vector Spaces](VectorSpaces.html)

$\mathbb{R}^n$ describes a vector of $n$ real numbers. Vectors can be *rows* or *columns*. A row vector corresponds (somewhat) to a $1 * n$ matrix. A column vector corresponds to a $n * 1$ vector.

Addition
---------------

* Vectors must be the same size.
* Add corresponding positions.
* ie. same as matrices.

Subtraction
--------

Add the *negative vector* (vector with the same magnitude but in the opposite direction).


Scalar multiplication
------------------

* Multiply each item by the scalar value.
* ie. same as matrices.

If one vector is a scalar multiple of another then they are *collinear* and *parallel*.

Norm (magnitude/length) of a vector
--------

Determined by pythagora's theorem.

$$ ||u|| = \sqrt{{u_1}^2 + {u_2}^2 + ... + {u_n}^2} $$

Observation: $||u|| = u . u$

Distance between vectors
--------

Distance between vectors $u$ and $v$ can be defined as the distance between their *terminal points* if their *initial points* are set equal. It is the *norm* of their differences.

$$ d(u,v) = ||u-v|| = \sqrt{({u_1}-{v_1})^2 + ... + ({u_n}-{v_n})^2} $$

Unit vector
-----------

Vector of length $1$ ($\Vert u \Vert = 1$).

To find a unit vector in the direction of $v$:

$$ u = \frac{v}{\Vert v \Vert} $$

Vector products (Euclidean inner product or dot product)
----------

$$ u . v = u_{1}v_{1} + ... + u_{n}v_{n} $$

Can be thought of as matrix multiplication as, $u^t . v$.

Vector products are:

* commutative
* distributive
* orthogonal if $u . v = 0$

Cross product
------

Written $u \: x \: v$. Only defined for vectors in 3-space. The result is a vector in 3-space. To find:

1. form the matrix

$$ \left( \begin{array}{ccc}
{u_1} & {u_2} & {u_3} \\
{v_1} & {v_2} & {v_3} \end{array} \right) $$

2. the first value is the determinant of the 2nd and 3rd columns.

3. the second value is $-1 x$ the determinant of the 1st and 3rd columns.

4. the third value is the determinant of the 1st and 2nd columns.

The cross product $u \: x \: v$ is orthogonal to both $u$ and $v$.

Two vectors are parallel if their cross product is zero. $u x v = 0$.

Alternative formula:

$$ a \: x \: b = \Vert a \Vert \: \Vert b \Vert \: sin(\Theta) \: \hat{n} $$

where $\theta$ is the angle between $a$ and $b$ and $\hat{n}$ is a unit vector perpendicular to the plane of $a$ and $b$.

Geometric Vectors
------

Have direction and magnitude. Start and end are called *initial point* and *terminal point*.

The vector with initial point $A$ and terminal point $B$ can be written:

$$ v = \vec{AB} $$

Vectors with the same length and direction are said to be *equivalent* and *equal*, even if they are in different positions.

The components of vector $v$ are the coordinates of its *terminal point* when the *initial point* is the origin of the coordinate system.

The *components* of a vector $\vec{AB}$ where $A=(a_1,a_2)$ and $B=(b_1,b_2)$ are $(b_1 - a_1, b_2 - a_2)$.

### Zero Vector

The vector with length $0$. Has no direction.

Angles Between Vectors
-----------

The angle ($\theta$) between the vectors $u$ and $v$ is:

$$ cos \theta = \frac{u \cdot v}{\Vert u \Vert \Vert v \Vert} $$

$$ \theta = cos^{-1}(\frac{u \cdot v}{\Vert u \Vert \Vert v \Vert}) $$

If $u \cdot v > 0$ then $u$ and $v$ make an acute angle.

If $u \cdot v < 0$ then $u$ and $v$ make an obtuse angle.

Vector Projection
--------

The projection of $u$ along $v$, or the component of $u$ parallel to $v$ is

$$ proj_v u = \frac{u \cdot v}{\Vert v \Vert^2}v $$

$proj_v u$ is parallel to $v$.

The remnant of u is:

$$ w = u - proj_v u $$ and is orthogonal to $v$.

Scalar projection
----

The length of the vector projection.

$$ comp_v u = \frac{u \cdot v}{\Vert a \Vert} $$

Area of Triangles
--------

$$ A = \frac{1}{2} \Vert PQ \Vert \Vert PR \Vert \: sin(\theta) $$

$$ A = \frac{1}{2} \Vert PQ x PR \Vert $$

Linear Combinations
---------------

Sums of scalar products of vectors.

$$ u = c_1v_1 + ... + c_nv_n $$

To determine if a vector is a linear combination of some set of vectors solve for the constants.

Span of a set of vectors
-----------

With a given set of vectors, how much of a vector space can we construct?

$$ span\{v_1,...,v_n\} = \{c_1v_1,...,c_nv_n\} $$

If $v_1,...,v_n$ span $V$ then every vector in $V$ can be expressed as a linear combination of $v_1,...,v_n$.

Basis Vectors
-----------

Instead of specifying a vector as the line segment from the origin to a point, we can instead specify the vector as the sum of scalar multiples of non-coplanar unit vectors (the basis vectors). E.g.

The vector $(3,7,10)$ is $3i + 7j + 10k$ if $i,j,k$ are unit vectors along the $x,y,z$ axis.

Formally, a set of vectors are a basis of a vector space if they span the vector space and are linearly independent.

If $V$ is an n-dimensional vector space then any set of n linearly independent vectors is a basis of $V$.

### How to construct a basis of a vector space?

For a vector space $V$:

* Chose an arbitrary vector $v_1 \in V$.

* If $\{ v_1 \}$ spans $V$ then it is a basis of $V$.

* Else add another vector $v_2 \in V \notin span \{ v_1 \}$.

* If $\{ v_1, v_2 \}$ spans $V$ then it is a basis of $V$. Else continue.

Coordinate Vectors
-----

Express a vector of a vector space in terms of a different basis of the vector space. For basis $B = \{v_1,v_2,...,v_n\}$ and vector $u$:

$$ u = c_1v_1 + c_2v_2 + ... + c_nv_n $$

$$ \left( \begin{array}{c}
c_1 \\
c_2 \\
... \\
c_n \end{array} \right) $$

is the coordinate vector of $u$ with respect to the basis $B$ ($[u]_B$).
