Poisson Distribution
===

Discrete events over a continuous interval. Successes must be independent.

E.g. counts per interval time

Single parameter is $\lambda$, the average or expected number of successes per unit.

$$ P(X=x) = \frac{e^{-\lambda}\lambda^x}{x!}$$

### Using R

To calculate "probabilities" Poisson with mean `m` (`P(X=x)`)

    dpois(x,lambda = m)

Poisson `P(X<=x)`

    ppois(x, lambda = m, lower.tail = TRUE)

Poisson `P(X>x)`

    ppois(x, lambda = m, lower.tail = FALSE)
