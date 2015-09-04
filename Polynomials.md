Binomials
-----

A binomial is a polynomial which is the sum of two terms (each a monomial).

**Perfect squares**

    (a + b)^2 = a^2 + 2ab + b^2
    (a - b)^2 = a^2 - 2ab + b^2

### Binomial Theorem

Starts from the perfect squares above and produces an expansion for higher degree binomials, e.g. `(a + b)^4`.

http://www.mathsisfun.com/algebra/binomial-theorem.html

    (a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k}b^k = \sum_{k=0}^n \frac{n!}{k!(n-k)!} a^{n-k}b^k

<img src="img/binomialtheorem.gif"/>

The coefficients can also be derived from **Pascal's Triangle**.

Quadratics
----

A quadratic is a degree 2 polynomial. To solve express as an equation = 0

    ax^2 + bx + c = 0

factor to `(x + z)(x + y) = 0` and observe that either `(x + z) = 0` or `(x + y) = 0` and, therefore, `x = -z` or `x = -y`. Alternatively, apply the quadratic formula:

    x = (-b +/- sqrt(b^2 - 4ac)) / 2a

### The Discriminant

The radical part of the quadratic formula `b^2 - 4ac` is called the **discriminant**. It determines how many solutions (roots) the equation has.

    if > 0 -> the equation has two real roots
    if = 0 -> the equation has one real root
    if < 0 -> the equation has no real roots.

Quadratic equations with no real roots cannot be factored and are called **irreducable**.

<script>
Q>>> How many roots does the following equation have? $$ x^2 + x + 2 $$ <<<
A>>> $$ b^2 - 4ac = 1 - 4*2 = -7 $$ since $$ -7 < 0 $$ therefore the equation has no real roots. <<<

Q>>> How many roots does the following equation have? $$ 5x^2 + 3x - 3 $$ <<<
A>>> $$ b^2 - 4ac = 9 - 4 * 5 * -3 = 69 $$ and $$ 69 > 0 $$ therefore the equation has 2 real roots. <<<
Q>>> What is the maximum number of turning points that the polynomial $$ f(x) = 3x^4 - 2x^5 + 19 $$ could have? <<<
A>>> The degree of the polynomial minus 1 = `5-1 = 4`  <<<
</script>

Factoring
----

### Factoring quadratics.

    ax2 + bx + c = 0

Find x and y such that `xy = ac` and `x + y = b`. If c is negative then x or y must be negative.

#### Difference of 2 squares

    a^2 - b^2 = (a - b)(a + b)

<script>
Q>>> $$ a^2 - b^2 = ? $$ <<<
A>>> $$ a^2 - b^2 = (a - b)(a + b) $$ <<<
</script>

#### Perfect squares

    a^2 + 2ab + b^2 = (a + b)^2
    a^2 - 2ab + b^2 = (a - b)^2

<script>
Q>>> $$ (a + b)^2 = ? $$ <<<
A>>> $$ (a + b)^2 = a^2 + 2ab + b^2 $$ <<<
Q>>> $$ (a - b)^2 = ? $$ <<<
A>>> $$ (a - b)^2 = a^2 - 2ab + b^2 $$ <<<
</script>

#### Perfect cubes

    a^3 + b^3 = (a + b)(a^2 - ab + b^2)
    a^3 - b^3 = (a - b)(a^2 + ab + b^2)

<script>
Q>>> $$ a^3 + b^3 = ? $$ <<<
A>>> $$ a^3 + b^3 = (a + b)(a^2 - ab + b^2) $$ <<<
Q>>> $$ a^3 - b^3 = ? $$ <<<
A>>> $$ a^3 - b^3 = (a - b)(a^2 + ab + b^2) $$ <<<
</script>

### Factoring 3rd degree polynomials

Factor by grouping. Group into two expressions. Extract common factors from each group. Try to make remaining expressions match.

### Factoring 4th degree polynomials

https://www.khanacademy.org/math/algebra2/polynomial_and_rational/factoring-higher-deg-polynomials/v/factoring-special-products-2

Theorems
------

### Remainder Theorem

http://www.mathsisfun.com/algebra/polynomials-remainder-factor.html

    f(x) / (x - c) = q(x) + r
    r = f(c)

### Factor Theorem

   if f(c) = 0 then x - c is a factor of f

This happens because (from the remainder theorem) `f(c) = 0` means the `f(x) / (x-c) = q(x) (remainder = 0)`.

Rational Functions
----

Ratios of polynomials. e.g.

    p(x) / q(x)
