Random Variables
=======

A experiment outcome that cannot be known in advance. E.g.

Experiment:       Toss coin 10 times
Random Variable:  # of heads
Outcome:          7 heads, 3 tails

`Random` seems a bit misleading, since we can know the probability of particular outcomes. We call a phenomenon random if individual outcomes are uncertain.

By convention, the random variable itself is given an upper-case identifier (`X`), while a particular instance of the random variable is given a lower-case identifier (`x`).

### rangespace

    The set of possible values that a random variable may take.

### Expected Value (`E(x)`)

The mean of the random variable.

$$ E(x) = np $$

### Probability Function

`f(x)` or `P(X=x)`. A function that gives the probability of particular outcomes. Continuing the earlier example (`X` = # of heads) P(X=7) is the probability of getting 7 heads in 10 coin tosses.

### Cumulative Distribution Function

    F(x) = P(X <= x)

Relies on some sequence of outcomes. The function gives the cumulative probability of the current outcome plus all the come before it.

Continuous Random Variables
------------

Values are not discrete. Distribution is specified by a probability density function (curve with an area = 1).

The probability that X is between two values is given by the area under the curve between those two values.

One distribution of continuous random variables is the [normal distribution](NormalDistribution).
