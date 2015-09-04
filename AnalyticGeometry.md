Point-slope form
---

Useful for finding the slope (`m`) of a graph or function. Also, for finding the function given two points.

    y - y' = m (x - x')

This is a reformulation of `m = delta y / delta x`

2 point form
-----

Point slope form with the definition of `m` subbed in.

    y - y' = (y'' - y')(x - x') / (x'' - x')

Odd / Even Functions
----

### Even Functions

Even function is symmetrical about the y axis.

    f(-x) = f(x)

e.g. `x^2`

<script>
Q>>> Is $$ f(x) = |x| $$ an odd function or an even function? <<<
A>>> $$ f(-x) = f(x) $$ therefore $$ f(x) = |x| $$ is an even function. <<<
</script>

### Odd Functions

Odd functions are symmetrical about the origin (180 degree rotational symmetry).

    f(-x) = -f(x)

e.g. `x^3`

<script>
Q>>> Is $$ f(x) = x^3 $$ and odd function or an even function? <<<
A>>> $$ f(-x) = -f(x) $$ therefore $$ f(x) = x^3 $$ is an odd function. <<<
</script>

To test for odd/even functions substitute `-x` for `x` (ie solve `f(-x)`) to `-f(x)` (odd) or `f(x)` (even).  

If all powers are even, then the function is even.

<script>
Q>>> Is $$ f(x) = 4x^4 + 3x^2 + 17 $$ an odd function or an even function? <<<
A>>> All the powers are even, therefore $$ f(x) = 4x^4 + 3x^2 + 17 $$ is an even function. <<<
</script>

If all powers are odd, then the function is odd.

<script>
Q>>> Is $$ f(x) = 4x^5 + 3x^3 + 5x $$ an odd function or an even function? <<<
A>>> All the powers are even, therefore $$ f(x) = 4x^5 + 3x^3 + 5x $$ is an odd function. <<<
</script>

If there is a mixture of odd and even powers then we have to test by substitution.

Shifting and Scaling Graphs
----

### Translations (shifts)

`f(x) + a` shifts the graph up by `a`.

`f(x + a)` shifts **left** by `a`.

<script>
Q>>> What is the relationship between the graphs of $$ f(x) = (x)^3 $$ and $$ f(x) = (x + 7)^3 $$? <<<
A>>> $$ f(x) = (x + 7)^3 $$ is $$ f(x) = (x)^3 $$ shifted left by 7. <<<
</script>

### Stretching

`af(x)` scales vertically by `a` i.e. every y value is multiplied by `a`.

<script>
Q>>> What is the relationship between the graphs of $$ f(x) = x^2 $$ and $$ f(x) = 2x^2 $$? <<<
A>>> $$ f(x) = 2x^2 $$ is $$ f(x) = x^2 $$ scaled vertically (every y value doubled).<<<
</script>

`f(ax)` scales horizontally by `1/a`.

<script>
Q>>> What is the relationship between the graphs of $$ f(x) = x^2 $$ and $$ f(x) = (2x)^2 $$? <<<
A>>> $$ f(x) = (2x)^2 $$ is $$ f(x) = x^2 $$ scaled horizontally by $$ 1/2 $$.
<img src="x2-2x2-(2x)2.png" /><br/>
$$ x^2, 2x^2, (2x)^2 $$<<<
</script>

### Reflection

The graph of `-f(x)` is the graph of `f(x)` reflected about the x-axis, because every point `(x,y)` becomes `(x,-y)`.

<script>
Q>>> What is the relationship between the graphs of $$ f(x) = x^2 $$ and $$ f(x) = -x^2 $$? <<<
A>>> $$ f(x) = -x^2 $$ is $$ f(x) = x^2 $$ reflected about the x-axis. <<<
</script>

The graph of `f(-x)` is the graph of `f(x)` reflected about the y-axis.

Drawing Graphs
----

1. Factorise (top and bottom for rational functions) if possible

1. (Optional) Determine if odd or even

1. Find y intercept

1. Find x intercepts

1. Find discontinuities (for rational functions this is divisor = 0)

1. Find limits (one-sided limits for all sides of all disconuities and limits +- \infty)

1. Determine sign in each interval between x intercepts and discontinuities.

Point of Inflection
-------

The point at which the sign of the curvature changes ie. the point where the sign of the derivative changes. Think of it as the point when the direction of turning changes.

To find the point of inflection, solve the second derivative for y=0. In the picture below, this is the point where the green line crosses the x-axis. Note that it corresponds to the point point where the original function (`f`) turns.

In maple

    f:=x^3-2*x^2-x+2
    plot([f,diff(f,x),diff(diff(f,x))],x = -2 .. 3, y = -5 .. 5, color = [red, blue, green])

<img src="img/inflection.png"/>

Three-dimensional Geometry
=====

### Symmetric equation of a line in 3d

$$ \frac{x - x_1}{a} = \frac{y - y_1}{b} = \frac{z - z_1}{c} = t $$

### Parametric equation of a line in 3d

Rearranging the symmetric equation to:

$$ x = x_1 + at $$
$$ y = y_1 + bt $$
$$ z = z_1 + ct $$

### Vector equation of a line

$$ R - R_1 = tl $$

$R$ and $R_1$ are vectors from the origin to points on a line. $l = ai + bj + ck$ is a vector parallel to the line. $t$ is a scalar.

This can be used to find the equation for a line from a point ($P_1$) and the direction of the line $l$.

Finding the equation of a line from two points.
----

1. Take the difference of the vectors corresponding to the two points. This gives the vector connecting the points, which defines the direction of the line ($l$).

1. This use the vector equation of the line with either point.

Planes
====

Planes are specified by a point in the plane and a vector orthogonal to the plane (*normal vector*).

Normal equation of a plane
-------

$$ Ax + By + Cz = D $$

$A,B,C$ are the *direction numbers* of the normal to the plane (vector perpendicular to the plane).

Perpendicular distance from origin
----

$$ d = \frac{|D|}{\sqrt{A^2 + B^2 + C^2}} $$

Where $|D|$ is the absolute value of $D$. $A,B,C$ are the direction numbers of the normal to the plane. I.e. the normal vector is $n = Ai + Bj + Ck$.

Vector Equation of a plane
---------------

$$ (R - R_1) \cdot n = 0 $$

Level Curves
----

A level curve is a set of points on the xy plane for which the value
$f(x,y)$, is constant. Try $f(x,y)=0, f(x,y)=1$ etc.

Limits of functions of two variables
-------------------

Limits can be added, multiplied and divided. Try substitution first. If the limit is $\frac{0}{0}$ this is indeterminate, and other techniques are required.
