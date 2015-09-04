Binomial Distribution
===

### The Binomial Distribution

The distribution of the number of successes in $n$ independent yes/no experiments, each of which yields success with a probability $p$.

> The probability of a 'number of heads' in 10 experiments of a coin toss is a binomial distribution, with $n = 10$ and $p = 0.5$.

### Binomial Probability

Recall:

Experiment:       Toss coin 10 times
Random Variable:  # of heads
Outcome:          7 heads, 3 tails

$$ P(X = x) = {n \choose x}p^x(1-p)^{n-x} $$

therefore, `X = # of heads, x = 7, n = 10, p=0.5`

$$ P(X = 7) = {10 \choose 7}0.5^70.5^3 =  $$

Explanation:

$0.5^7 * 0.5^3$ is the probability of any one way of getting 7 heads out of 10, e.g. HHHHHHHTTT or TTTHHHHHHH. ${10 \choose 7}$ is the number of ways in which 7 heads out of ten can occur.

### Using TI-nspire

TI-nspire has this function as binomPdf(n, p, x). (not case sensitive). Also has nPr and nCr functions.

### Using R

To calculate "probabilities" (`P(X=x)`) where X is `number of heads` and `x = 7`.

    dbinom(x,n,p)
    dbinom(7,10,0.5)

To calculate "tail probabilities" (`P(X<=1)`)

    pbinom(1,10,.5)

P(X>1)

    pbinom(1,10,.5,lower.tail=FALSE)

Poisson with mean `m` (`P(X=x)`)

    dpois(x,lambda = m)

Poisson `P(X<=x)`

    ppois(x, lambda = m, lower.tail = TRUE)

Poisson `P(X>x)`

    ppois(x, lambda = m, lower.tail = FALSE)
