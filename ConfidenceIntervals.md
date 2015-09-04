Confidence Intervals
------

Confidence intervals state how trustworthy our inferences about a population are.

Give, or assuming $\bar{x}$ is normally distributed we can give a confidence interval by relying on the normal distribution.

### 95% confidence interval

The 95% confidence interval is the range of values within which we are 95% confident that the population mean ($\mu$) lies.

$$ \bar{x} \pm 1.96 \frac{\sigma}{\sqrt{n}}$$

For other population means replace `1.96` with the appropriate value, found by looking at the 9999 degrees of freedom row of the T-distribution tables for $P=\frac{1-\frac{percentage}{100}}{2}$.

Note that this requires knowing the population standard deviation ($\sigma$).

### General Formulation

A confidence interval, generally, is:

$$ \bar{x} \pm \text{margin of error} $$

Where `margin of error` is:

$$ Z^* \frac{\sigma}{\sqrt{n}}$$

$Z^*$ is whatever the critical value is. The other factor is the **standard error** (denominator of the test statistic).

### Confidence Interval with $\sigma$ is unknown

If $\sigma$ is unknown we use $s$, and instead of using the `9999` degrees of freedom we use $n-1$ degrees of freedom for the t-distribution.

$$ \bar{x} \pm t^*_{n-1} \frac{s}{\sqrt{n}} $$

NOTE: All of this requires $n>30$ of confirmation that $\bar{x}$ is normally distributed via a QQ Normal Plot.

**Required Assumptions**

* the data be approximately normal
* the data be relatively symetrical
* the data be unimodal
* the data have no outliers
* the sample be taken randomly

Confidence Intervals for Population Proportions
---

$$ p = \text{population proportion} $$

$$ \hat{p} = \text{sample proportion} $$

Confidence interval is still

$$ \hat{p} \pm z^* \text{standard error} $$

but now the standard error is

$$ \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} $$

NOTE: To satisfy the required assumptions $n\hat{p} >5$ and $n(1-\hat{p}) > 5$.

### Using R

    prop.test(x, n, conf.level=0.95, correct=F)

Where `x` is the number of successes, `n` is the size of the sample. The result includes a confidence interval.

Sample Size for Required Margin of Error (Quantitative Data)
---

We can determine the required sample size (`n`) for a given margin of error (`m`) by:

$$ n = (\frac{z^*\sigma}{m})^2 $$

Sample Size for Required Margin of Error (Qualitative Data)
---

$$ n = (\frac{z^*}{m})^2 p(1-p) $$

### Confidence Intervals for 2 Samples

If 0 is in interval, then there is no significant differences in the groups
