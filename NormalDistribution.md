Normal Distribution
====

Also called Gaussian distribution. Bell shaped. Described by mean (center) and standard deviation.

Often written as N(mean, variance)

68% of observations fall within 1 standard deviation of the mean.

95% of observations fall within 2 standard deviations of the mean.

99.7% of observations fall within 3 standard deviations of the mean.

Standard Normal Distribution
----

$$ N(0,1) $$

### Z Score

How many standard deviations away from the mean is a value?

$$ Z = \frac{X - \mu}{\sigma} $$

<script>
Q>>> The `Z-score` is ... <<<
A>>> The 'standard score' or number of standard deviations a datum is above the mean. A negative value indicates the value is below the mean. <<<
Q>>> $$ Z = \text{?} $$ <<<
A>>> $$ Z = \frac{X-\mu}{\sigma} $$ <<<
</script>

### Using R

Use the normal distribution to find the probability of a variable being less than z. Value to probability.

    pnorm(z, mean, sd)

Use the normal distribution to find the value having a probability that the variable will be less than it of 5%. ie. Probability to value.

    qnorm(0.05, mean, sd)

or

    qnorm()

### QQ Plot

Plot of a sample against the normal distribution designed to show how normal the data is. A normally distributed data set will follow the diagonal line (x=y).
