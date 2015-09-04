[Statistics](Statistics.html)

Exponential Distribution
=====

Waiting interval between two successes in a Poisson distribution has an exponential distribution.

Or, how long something lasts for where the chance of failure at any instant stays the same. (bull riding?)

$\alpha =$ average number per unit of time $\therefore \frac{1}{a} =$ average time

$$ P(T \leq t) = 1 - e^{-\alpha t} $$

### Using R

`P(X > 3)` where $\alpha = 2$ therefore rate = $1/2$

    pexp(3, rate=1/2, lower.tail=FALSE)

### Memoryless property

The exponential distribution has the memoryless property, meaning that any time already waited does not effect the probability of an event occuring in the next $t$ units of time.
