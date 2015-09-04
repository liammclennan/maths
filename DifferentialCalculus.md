[Calculus](Calculus.html)

Differential Calculus
====

The derivative is the instantaneous rate of change of a function at a point. Also, the slope of the line tangent to that point.

The derivative (at a point) is the limit of `Δy/Δx` as the range `Δx` becomes arbitrarily small.

Thus, $f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$

The derivative only exists if a suitable limit exists. Functions have derivatives if:

1. It is continuous

1. It is smooth (no corners). (Unlike f(x) = |x|)

Polynomial Derivatives
---

$$\frac{dx^n}{dx} = nx^{n-1}$$

<script type="flashcard">
Q>>> What is the derivative of $$ 7x^4 $$? <<<
A>>> $$ 28x^3 $$ <<<
</script>

### Constants

The derivative of a constant is `0`.

$$\frac{dc}{dx} = 0$$

This can be found from the derivative of polynomials, since $5 = 5x^0 -> 0 * 5x^-1 = 0$.

<script type="flashcard">
Q>>> What is the derivative of $$ 99 $$? <<<
A>>> $$ 0 $$ because $$ 99 = 99x^0 = 0 * 99x^-1 = 0 $$ <<<
</script>

### Product Rule

    (uv)' = uv' + u'v

<script type="flashcard">
Q>>> Where `u` and `v` are functions $$ (uv)' = ? $$ <<<
A>>> $$ (uv)' = uv' + u'v $$ <<<
</script>

### Quotient Rule

<img src="http://latex.codecogs.com/gif.latex?%28%5Cfrac%7Bu%7D%7Bv%7D%29%27%20%3D%20%5Cfrac%7Bvu%27%20-%20v%27u%7D%7Bv%5E2%7D"/>

> (\frac{u}{v})' = \frac{vu' - v'u}{v^2}

Note:

* the function `u` is differentiated first in the subtraction in the dividend.
* The divisor is the original divisor squared.

<script type="flashcard">
Q>>> $$ (\frac{u}{v})' = ? $$ <<<
A>>> $$ (\frac{u}{v})' = \frac{vu' - v'u}{v^2} $$ <<<
</script>

### Chain Rule

$$\frac{d}{dx} f(g(x)) = f'(g(x))g'(x) $$

<script type="flashcard">
Q>>> $$ \frac{d}{dx} f(g(x)) = ? $$ <<<
A>>> $$ \frac{d}{dx} f(g(x)) = f'(g(x))g'(x) $$ <<<
</script>

Implicit Differentiation
------

A function defined by a relation is said to be defined implicitly. E.g. `x^2 + y^2 = 0`

To find the derivative (`dy/dx`) differentiate both sides of the equation with respect to `x`, remembering that `y = y(x)`.

Given that `y` is a function, solutions are likely (certain?) to involve the chain rule.

Related Rates
-----

1. Write down the known values

1. Express the relationship between the known quantities.

1. Differentiate both sides and solve.

E.g. Square dl/dt = -2 and dw/dt = 2. When l = 12 and w = 5.

    A = l * w
    dA/dt = dl/dt w + dw/dt l (by product rule)
    dA/dt = -2*5 + 2*12
          = 14 cm^2/s increasing

Linear Approximation
------

If we have `f(a)` but want `f(a+b)` we can use linear approximation.

    L(a+b) = f(a) + f'(a)b
    or
    L(x) = f(a) + f'(a)(x-a)

Stationary Points
-----

$$ f'(x) = 0 $$

Represent a horizontal line. Give local minimums and maximums of smooth curves.

If $f''(x) < 0$ then it is a local max.

If $f''(x) > 0$ then it is a local minimum.

If $f''(x) = 0$ and $f'''(x) \neq 0$ then it is a **horizontal inflection point** (as for $x^3$).

Local min and max can also occur where f'' is not defined (corners) or endpoints.

<script>
Q>>> $$f'(2) = 0$$. What does this tell us? <<<
A>>> That the slope of f is 0 at x = 2, therefore x=2 is a turning point or horizontal point of inflection. <<<
Q>>> $$f'(2) = 0$$ and $$f''(2) = -4$$. What does this tell us? <<<
A>>> $x = 2$ is a local maximum, because $$f'(2) = 0$$ tells us it is a turning point or a point of inflection, and $$f''(2) < 0$$ tells us it is concave down.<<<
</script>

Concavity
----

The **concavity** of a curve is given by the double derivative (f'').

Where $ f''(x) < 0$ then concave down.
Where $ f''(x) > 0$ then concave up.

Point of Inflection
----

Where the concavity changes sign, that is, where $f''$ crosses the x axis. This is where $f''(x) = 0$ and changes sign about the point (generally when $f'''(x) \neq 0$).

<script>
Q>>> What are the two requirements for a point of inflection?  <<<
A>>> A point of inflection is defined as a point where the concavity changes. The requirements are:

1. $$f''(x) = 0$$

1. f'' changes sign about the point ($$f'''(x) \neq 0$$). <<<
</script>

Newton's Method
----

If $x_0$ is a guess for a solution for $f(x) = 0$ then a better guess might be:

$$ x_1 = x_0 - \frac{f(x_0)}{f'(x_0)} $$

<script>
Q>>> if $$x_0$$ is a guess for a root of the function `f`, Newton's method suggests that a better guess is...  <<<
A>>> $$x_1 = x_0 - \frac{f(x_0)}{f'(x_0)}$$ <<<
</script>
