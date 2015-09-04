Sampling Distributions
===

A 'sample' is a subset of a population, hopefully chosen randomly.

$n$ indicates the number of elements in the sample.

$X_1, X_2,...$ represent individual elements in the sample before their values are known.

$x_1, x_2,...$ indicate individual elements of the sample after their values are known.

Sample Metrics
----

Sample Mean

$$ \bar{X} = \frac{\sum_i{X_i}}{n}$$

Sample Variance

$$ S^2 = \frac{\sum_i{(X_i-\bar{X})^2}}{n-1} $$

These metrics are functions of random variables, also known as **statistics**. Because they are functions of random variables, they are also random variables.

The standard deviation of a statistic is called its **standard error** and is defined as:

$$ SE = \frac{\sigma}{\sqrt{n}} $$

The Sample Mean ($\bar{X}$)
---

If the population is normally distributed, or $n > 30$ (due to central limit theorem) then the sample mean ($\bar{X}$) will be normally distributed ($N(\mu,\frac{\sigma}{\sqrt{n}})$).

The Sample Proportion ($\hat{p}$)
---

The sample mean is only sensible for quantitative data. For qualitative data use the sample proportion. This is the proportion of "successes" in the sample.

$$ \hat{p} = \frac{\text{number of successes}}{n} $$

> If we observe $n$ independent trials, each having probability $p$ or being a 'success' then

$$ Z = \frac{\hat{p} - p}{\sqrt{\frac{p(1-p)}{n}}} $$

For $n$ to be large enough for the distribution of $Z$ to approximate normal we require $np>5$ and $n(1-p)>5$.
