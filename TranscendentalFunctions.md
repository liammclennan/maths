Transcendental Functions
===

Transcendental functions are those other than the polynomials.

Exponential Functions
---

$$ f(x) = a^x $$

where a is a constant. Always have y-intercept at (0,1) (because $a^0 = 1$ for all `a`). Larger values of `a` make the curve steeper.

```{r}
library(ggplot2)
twoToX <- ggplot(data.frame(x=c(-2,2)), aes(x)) + stat_function(fun=function(x)2^x, geom="line", aes(colour="2^x"))
twoToX + stat_function(fun=function(x)4^x, geom="line", aes(colour="4^x"))
```

The function $f(x) = e^x$ has $slope = 1$ at $x = 0$. The value of $e$ is

```{r}
exp(1)
```

Inverse Functions
----

Inverse functions are such that $$f^{-1}(f(x)) = x$$ also
$$(f^{-1} \circ f)(x) = x$$
$$(f \circ f^{-1})(x) = x$$

That is, the inverse function $f^{-1}$ 'undoes' the function $f$.

Graphically, inverse functions are reflected about $y=x$.

```{r}
library(ggplot2)
twoToX <- ggplot(data.frame(x=c(-1,1)), aes(x)) + stat_function(fun=function(x)2*x, geom="line", aes(colour="2x"))
twoToX + stat_function(fun=function(x)0.5*x, geom="line", aes(colour="x/2")) + stat_function(fun=function(x)x, geom="line", aes(colour="x"))
```

### Horizontal Line Test

A function can be inverted if no horizontal line would cross its plot twice. Therefore, $y=2x$ is invertible and $y=x^2$ is not. Often functions are only invertible over a certain domain.

To find a function's inverse reverse the input and output e.g.

let $y = 2x$ then $x = 2y$ and $y = \frac{x}{2}$

Logarithms
---

The inverse of the exponential functions $y = a^x$ are the logarithms (base a) $x = log_a y$. Logarithms base $e$ are special and written $\ln x$

### Log Laws

$$ \log(xy) = \log(x) + \log(y) $$
$$ \log(\frac{x}{y}) = \log(x) - \log(y) $$
$$ \log(a^n) = n\log(a) $$
$$ \log(1) = 0 $$
$$ log_{a}(b) = \frac{log_z(b)}{log_z(a)} \text{where z can be any base}$$
$$ \ln(e^x) = x $$

<script>
Q>>> $$\log(xy) = \text{?}$$ <<<
A>>> $$\log(xy) = \log(x) + \log(y) $$  <<<
Q>>> $$ \log(\frac{x}{y}) = \text{?} $$ <<<
A>>> $$ \log(\frac{x}{y}) = \log(x) - \log(y) $$ <<<
Q>>> $$ \log(a^n) = \text{?} $$ <<<
A>>> $$ \log(a^n) = n\log(a) $$ <<<
Q>>> $$ \log(1) = \text{?} $$ <<<
A>>> $$ \log(1) = 0 $$ <<<
Q>>> $$ log_{a}(b) = \text{?} $$ <<<
A>>> $$ log_{a}(b) = \frac{log_z(b)}{log_z(a)} $$ <<<
Q>>> $$ \ln(e^x) = \text{?} $$ <<<
A>>> $$ \ln(e^x) = x $$ <<<
</script>

Derivatives
---

$$ \frac{d}{dx} e^x = e^x $$
$$ \frac{d}{dx} a^x = (ln a)a^x $$
$$ \frac{d}{dx} f^{-1} = \frac{1}{f'(f^{-1})} $$

### Rules for differentiating logarithms

$$ \frac{d}{dx}  ln x = \frac{1}{x} $$
$$ \frac{d}{dx} log_a x = \frac{1}{x\ln a} $$

<script>
Q>>> $$ \frac{d}{dx} e^x = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} e^x = e^x $$ <<<
Q>>> $$ \frac{d}{dx} a^x = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} a^x = (ln a)a^x $$ <<<
Q>>> $$ \frac{d}{dx} f^{-1} = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} f^{-1} = \frac{1}{f'(f^{-1})} $$ <<<
Q>>> $$ \frac{d}{dx}  ln x = \text{?} $$ <<<
A>>> $$ \frac{d}{dx}  ln x = \frac{1}{x} $$ <<<
Q>>> $$ \frac{d}{dx} log_a x = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} log_a x = \frac{1}{x\ln a} $$ <<<
</script>

Exponential Growth and Decay
----

Models recursive processes, where the function output forms part of its input, e.g. compound interest, population growth etc.

Exponential growth is defined formally as

$$ \frac{dP}{dt} = kP $$

So the rate of change changes with the value. The higher (or lower) the value the higher (or lower) the rate of change.

and

$$ P = P_0 e^{kt} $$

If I know the population now ($P_0$), then the ratio of future population to current population ($P : P_0$) is $e^{kt}$.

<script>
Q>>> If a value grows exponentially what is the equation that describes the population in the future? <<<
A>>> $$ P = P_0 e^{kt} $$ <<<
Q>>> If a value decays exponentially what is the equation that describes the population in the future? <<<
A>>> $$ P = P_0 e^{-kt} $$ <<<
</script>

Inverse Trig Functions
----------

### $sin^{-1}$

Domain = $[-1,1]$
Range = $[\frac{-\pi}{2},\frac{\pi}{2}]$

The domain and range are determined by looking at a range of $sin$ that is invertible.

```{r}
curve(sin, 1.1*-pi/2,1.1*pi/2)
```

$sin$ is invertible for the domain $[\frac{-\pi}{2},\frac{\pi}{2}]$, so that becomes the range of $sin^{-1}$. The range of $sin$ in this domain is $[-1,1]$ so that becomes the domain of $sin^{-1}$.

```{r}
curve(asin, -1,1)
```

### $tan^{-1}$

Domain: $[-\infty,\infty]$
Range: $[\frac{-\pi}{2},\frac{\pi}{2}]$

The domain and range are calculated by choosing an invertible section of $tan$ (passes horizontal line test and includes the origin). The domain and range of $tan^{-1}$ are the range and domain of $tan$.

Derivatives of Inverse Trig Functions
------

$$ \frac{d}{dx} sin^{-1}(x) = \frac{1}{\sqrt{1-x^2}} $$
$$ \frac{d}{dx} cos^{-1}(x) = \frac{-1}{\sqrt{1-x^2}} $$
$$ \frac{d}{dx} tan^{-1}(x) = \frac{1}{1+x^2} $$

<script>
Q>>> $$ \frac{d}{dx} sin^{-1}(x) = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} sin^{-1}(x) = \frac{1}{\sqrt{1-x^2}} $$ <<<
Q>>> $$ \frac{d}{dx} cos^{-1}(x) = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} cos^{-1}(x) = \frac{-1}{\sqrt{1-x^2}} $$ <<<
Q>>> $$ \frac{d}{dx} tan^{-1}(x) = \text{?} $$ <<<
A>>> $$ \frac{d}{dx} tan^{-1}(x) = \frac{1}{1+x^2} $$ <<<
</script>

Hyperbolic Functions
----------------

$$ tanh x = \frac{cosh x}{sinh x} $$

### Identities

$$ cosh^2 x - sinh^2 x = 1 $$

$$ sinh 2x = 2 sinh x \: cosh x $$ 
