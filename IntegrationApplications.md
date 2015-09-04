Integration Applications
===========

Area
---

> Signed area is the integral

Method:

1. Find intersections
2. Calculate: $\int \text{part above x axis}- \int \text{part below x axis}$

### Area between f(x) and g(x)

$$ A = \int_a^b |f(x) - g(x)| \: dx $$ 

where $a$ and $b$ are points of intersection of the curves. 

Arc Length
----

$$ l = \int \sqrt{1 + (\frac{dy}{dx}})^2 dx $$

Averages
----

The idea is that the average value of a function between $a$ and $b$ is the integral of the function divided by the number of x values (sort of).

Average value of $y(x)$ between $a$ and $b$:

$$ \frac{\int_a^b \: y(x) \: dx}{\int_a^b \: 1 \: dx} $$

simplified:

$$ \frac{1}{b-a} \int_a^b y(x) \: dx $$

Volumes
-----

Basic strategy is to determine the volume of small pieces and integrate (sum) them.

If $A(x_i)$ is a function giving the area of the cross section at $x_i$ then the volume is: 

$$ V = \lim_{n\to\infty} \sum_{i=1}^nA(x_i)\Delta x$$
$$ V = \int_a^b A(x) \: dx $$

### General

$$ V = \int \pi r^2 dh  $$

### Rotating about x- axis

$$ V = \int \pi y^2 dx $$

### Rotating about y-axis 

$$ V = \int \pi x^2 dy $$

### Discs

Consider a function rotated about the x axis to form a 3d shape. 

```{r}
curve(x^1)
```

Vertical slices produce discs. The volume of a disc is:

$$ dV = \pi f(x)^2 dx $$

so

$$ V = \pi \int_a^b f(x)^2 \: dx $$

### Washers

$$ V = \pi \int {r_+}^2 - {r_-}^2 \: dh $$

### Shells

$$ V = 2\pi \int rh \: dr $$

Rotate about y-axis: $V = 2\pi \int xy \: dx$

Rotate about x-axis: $V = 2\pi \int yx \: dy$

