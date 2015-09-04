[Calculus](Calculus.html)

Integral Calculus
===

[Integration Applications](IntegrationApplications)

Antiderivative / Indefinite Integral
----

The antiderivative / indefinite integral of $f(x)$ is the function $F(x)$ which when differentiated gives $f(x)$.

$$ F'(x) = f(x) $$

Thus, the indefinite integral of $2x$ is $x^2$.

$$ \frac{d}{dx} x^2 = 2x $$

and

$$ \int 2x dx = x^2 + C $$

`C` is an unknown constant called the 'constant of integration'.

Integrating exponents and Coefficients
---

Reverse the rule for differentiating.

$$ \int x^n dx = \frac{x^{n+1}}{n+1} + C $$

> NOTE: This only works when $n \ne -1$

<script>
Q>>> What is $$\int 2x^5 dx$$ ? <<<
A>>> $$\frac{x^6}{3}$$ <<<
</script>

### Integrating $\frac{1}{x}$

$\frac{1}{x}$ is $x^{-1}$ thus the standard rule causes a divide by zero. Fortunately, we know from derivatives that $\frac{d}{dx} ln(x) = \frac{1}{x}$, therefore:

$$ \int \frac{1}{x} dx = ln|x| + C $$

> NOTE: The derivative of $ln(-x)$ is also $\frac{1}{x}$ (by the chain rule), hence the integral is $ln|x| + C$.

<script>
Q>>> What is $$\int \frac{1}{x} dx$$ ? <<<
A>>> $$ ln|x| + C $$ <<<
</script>

### Reverse Integral

$$ \int_a^b f(x) dx = - \int_{b}^{a} f(x) dx $$

Definite integrals are the signed area under the curve. Area above the x axis is positive, area below the x axis is negative. Thus, $\int_a^b sin(x) dx = 0$.

Fundamental Theorem of Calculus
----

Part 1:

Integration and differentiation are inverse operations. The derivative of an integral of a function, gives the function.

Part 2:

Definite integrals are the indefinite integral applied to the upper bound minus the indefinite integral applied to the lower bound. i.e.

$$ \int_a^b f(x) dx = (\int f(x) dx)(b) - (\int f(x) dx)(a) $$

Odd and Even Functions
----

Intuitively, $\int_{-a}^a$ of an even function is $2 * \int_0^a$.

$\int_{-a}^a$ of an odd function is $0$.

Warnings
---

* Only works over continuous intervals.

* Area under the curve is signed, so questions asking for the area between the curve and the x-axis have to be split at x intercepts. Then sum the absolute values of the individual areas.

Substitution Method
----

The basic procedure:

1. Choose a substitution ($u$)

1. Differentiate $u$ to get $\frac{du}{dx}$. Make $dx$ the subject of the equasion.

1. Substitute everything to get rid of $x$s.

1. Do the new integral, or do another substitution.

1. Replace $u$ by its value to get back to a function of $x$.

> NOTE: Don't forget to add the constant of integration ($+ C$).

Maple Integration
--------------

### Indefinite Integration:

    f1 := x^7-4*x^3+3;
                              7      3
                             x  - 4 x  + 3
    r1 := int(f1, x);
                            1  8    4
                            - x  - x  + 3 x
                            8

### Definite Integration

$$ \int_1^2 \frac{1}{(x+3)^3} + \frac{1}{x} dx $$

    f2 := 1/(x+3)^3+1/x;
                             1       1
                          -------- + -
                                 3   x
                          (x + 3)

    r2 := int(f2, x = 1 .. 2);
                               9
                              --- + ln(2)
                              800

Numerical Approximation
------

Not all integrals can be evaluated. In other cases we use numerical approximation, usually by dividing the area into $n$ fixed width panels.

The area of each panel can be approximated by considering them as rectangles or trapezoids.

### Trapezoidal Rule

$$ \int_a^b f(x) \: dx \approx \frac{b-a}{2}(f(a) + f(b)) $$

This can be used with panels by calculating them individually and adding the result. Given $n$ is the number of panels and $a = x1 < x2 < ... < xN+1 = b$ then:

$$ \int_a^b f(x) \: dx \approx \frac{b-a}{2n} \sum_{k=1}^n (f(x_{k+1}) + f(x_k)) $$

### Simpson's Rule

Uses quadratic polynomials to approximate the integral of a function, compared to the straight lines used by the Trapezoidal Rule.

$$ \int_a^b f(x) \: dx \approx \frac{b-a}{6}(f(a) + 4f(\frac{a+b}{2}) + f(b)) $$

Integration By Parts
------------------

Reverses the product rule. Given a product integral,

$$ \int uv' \: dx = uv - \int u'v \: dx $$

As multiplication is commutative we can choose which factor is $u$ and which $v'$.

Advice on choosing $u$ and $v'$:

* must be able to integrate $v'$
* must be able to differentiate $u$
* it helps if $u'$ is simpler than $u$
* it helps if $v$ is simpler than $v'$

### With Maple

```
intparts(f, u)
```

f - expression of the form Int(u*dv, x)

u - factor of the integrand to be differentiated

```
eq := Int(theta^2*sin(2*theta),theta);
eq1 := intparts(eq,theta^2);
eq2 := intparts(eq1,theta);
eq3 := value(eq2);
```

Integrals of trigonometric functions
---------

Use trig identities to make the expression easier to integrate.

$sin^2\theta + cos^2\theta = 1$ is useful.

Integrals of the form

$$ \int_{-\pi}^{\pi} sin(nx) cos(mx) \: dx $$

can be simplified using the identities:

$$ 2sin(A)cos(B) = sin(A+B) + sin(A-B)
 2cos(A)cos(B) = cos(A+B) + cos(A-B) $$
$$ 2sin(A)sin(B) = cos(A-B) - cos(A+B) $$

Trigonometric substitutions
----------

Substitute trig functions to use trig identities to make the expression easier to integrate.

Integrals of Rational Functions
--------------

Make a simpler expression by partial fraction decomposition. I.e. split the denominator to convert a product to a sum.

### Partial Fraction Decomposition

Split the denominator and create a sum of fractions, with variables for the numerators.

If the numerator is a higher order polynomial than the denominator start with long division.

### Case 1 Denominator is a product of distinct linear factors

$$ \frac{1}{(x-2)(x-5)} = \frac{A}{x-2} + \frac{B}{x-5} $$

Do the sum:

$$ A(x-5) + B(x-2) = 1 $$
$$ (A+B)x + (-5A-2B) = 1 $$

therefore:

$A+B = 0$ and $-5A-2B=1$ and

$$\frac{1}{(x-2)(x-5)}= \frac{1}{3} * (\frac{-1}{x-2} + \frac{1}{x-5})$$

### Case 2 Denominator is a product of linear factors, some of which are repeated

This is the case of $\frac{R(x)}{x^a \cdot y^b}$.

Include a term for $1..a$ and $1..b$ ie.

$$ \frac{A}{x} + ... + \frac{B}{x^a} + \frac{C}{y} + ... + \frac{D}{y^b} $$

### Case 3 Denominator contains irreducible quadratic factors, none of which is repeated

The partial fraction numerators *must be
the most general polynomial of lower degree than the denominator*. If the denominator is quadratic then the numerator will be linear. E.g.

$$ \frac{x+1}{x(x^2 + 1)} = \frac{A}{x} + \frac{Bx + C}{x^2+1} $$

Use $Ax + B$ for the numerator of terms instead of $A$ ie.

$$ \frac{R(x)}{(x^2 + 1)x} = \frac{A}{x} + \frac{Bx + C}{x^2 + 1} $$
