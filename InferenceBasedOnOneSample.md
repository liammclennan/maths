Inference Based on One Sample
=====

For quantitative data focus is on $\mu$ (the mean of the population).

For qualitative data the focus is on $p$ (the expected number of successes).

To estimate the mean of the population $\mu$ we use the mean of the sample $\bar{x}$. The quality of this estimate is described by the **standard error** ($\frac{s}{\sqrt{n}}$), or by a **confidence interval**.

[Confidence Intervals](ConfidenceIntervals)

One-sample Z test statistic
---

$$ Z = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0,1) $$

Then find the probability (assuming N(0,1)) of Z. This requires $n$ to be large (>30).

One-sample T test statistic
---

For single sample quantitative data we generally test the null hypothesis $H_0: \mu = \mu_0$. ie does the sample mean match the population mean within an allowed level of significance?

$$ t = \frac{\bar{X} - \mu_0}{\frac{S}{\sqrt{n}}} \sim t_{n-1} $$

NOTE: $S$ is the standard deviation of the **sample**.

#### Using R

    t.test(c(1,2,3,4,5,6,7,8,9,1,1,1),mu=7)
    One Sample t-test

    data:  c(1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 1, 1)
    t = -3.5178, df = 11, p-value = 0.004817
    alternative hypothesis: true mean is not equal to 7
    95 percent confidence interval:
    2.122994 5.877006
    sample estimates:
    mean of x
          4

To specify the type of comparison use `alternative = "two.sided" | "less" | "greater"`.

With a p-value of `0.004817` it is extremely unlikely that this sample came from a t-distribution with mean=7. Therefore, $H_0$ is rejected.

1-sample test of proportion
---

For a single sample of qualitative data. Requires:

$$ np > 5, n(1-p) > 5 $$

Test statistic is:

$$ Z = \frac{\hat{p} - p}{\sqrt{\frac{p(1-p)}{n}}} \sim N(0,1) $$

### Conditions for inference

* The data used for the estimate are an SRS from the population
studied
* if $np > 5$ and $n(1-p) > 5$ then (using Central Limit Theorem) Z has approximately a N(0,1) distribution.


<script>
Q>>> What is the standardising formula for proportions? <<<
A>>> $$ Z = \frac{\hat{p} - p}{\sqrt{\frac{p(1-p)}{n}}} \sim N(0,1) $$ <<<
Q>>> What is the test to determine if a qualitative sample can be considered normal? <<<
A>>> $$np > 5$$ and $$n(1-p) > 5$$ <<<
</script>

### Using R

    prop.test(# of successes, n, p, alternative = "two.sided" | "less" | "greater", correct=F)

The `correct` parameter is for continuity correction.

Example from slides:

    prop.test(137,500,.242,alternative="greater",correct=F)

    1-sample proportions test without continuity correction

    data:  137 out of 500, null probability 0.242
    X-squared = 2.7912, df = 1, p-value = 0.04739
    alternative hypothesis: true p is greater than 0.242
    95 percent confidence interval:
    0.2424737 1.0000000
    sample estimates:
    p
    0.274
