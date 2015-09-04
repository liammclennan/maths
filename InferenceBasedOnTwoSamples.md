Inference Based on Two Samples
===

Summary of Means
---

$\mu$ - population mean

$\bar{X}$ - mean of a random sample (a random number, that is normally distributed). The distribution of $\bar{x}$s.

$\bar{x}$ - mean of a particular sample ($\sum \frac{x}{n}$)

Comparing two populations or two samples is a common situation called a **two sample** problem. The two samples can be either **paired** or **independent**. 

Parameter notation:

| | Size | Mean | Variance |
|-|--|--|--|
|Population | N | $\mu$ | $\sigma^2$ |
|Sample|n|$\bar{x}$| $s^2$|

> NOTE: subscript indexes are used to differentiate populations and samples (e.g. $N_1$, $\bar{x}_2$)

### Independent Samples

Randomly assigned to the groups or no connection between groups.

### Paired Samples

Each individual in the first group is paired / matched to an individual in the second group. Samples must be the same size. 

<script type="flashcard">
Q>>> A experiment is run with two paired groups. Group 1 has 10 individuals. How many individuals are in group 2? <<<
A>>> 10. Paired groups require the same number of samples. <<<
</script>

Analysis of 2 Indedependent Quantitative Samples
===

**Two Populations** - We use a sample from each population to predict differences in the two populations.

The null hypothesis is 'no difference' ($H_0: \mu_1 = \mu_2$)

The test statistic for comparing the means of the two populations will be based on $\bar{x}_1 - \bar{x}_2$.

Welch 2-sample t-test (non-pooled t-test)
----

Compares the means of 2 independent, quantitative samples. Use when population variances are unequal.

$$ H_0: \mu_1 = \mu_2 $$

Test statistic and sampling distribution

$$ t = \frac{\bar{X}_1-\bar{X}_2-(\mu_1-\mu_2)}{\sqrt{\frac{s^2_1}{n_1} + \frac{s^2_2}{n_2}}} \sim t_{df} $$

> NOTE: the formula for df is big and ugly

### Conditions required for Welch 2-sample t-test

* Two groups are independent 
* Data is quantitative
* Comparison is of population means
* Each group is drawn from a normal population

Pooled t-test
----

Compares the means of 2 independent, quantitative samples. Use when population variances are equal. Gives narrower confidence interval that Welch t-test, hence more powerful (less likely to fail to reject an incorrect $H_0$).

Estimate the common variance (weighted average of the sample variances):

$$ {s_p}^2 = \frac{(n_1-1){s_1}^2 + (n_2-1){s_2}^2}{n_1 + n_2 - 2} $$

The test statistic and sampling distribution are:

$$ t = \frac{\bar{x}_1 - \bar{x}_2 - (\mu_1 - \mu_2)}{\sqrt{{s_p}^2(\frac{1}{n_1} + \frac{1}{n_2})}} \sim t_{n_1 + n_2 - 2} $$

### Using R

    t.test(saliva.pH~sample, alternative='two.sided', conf.level=.95, var.equal=TRUE, data=saliva)

Comparing Population Variances (F-test of variance)
----

Infer population variance equality from sample variances by using an F-test of variance. Used to choose between a Welch t-test (when population variances are not equal) and a pooled t-test (when population variances are equal). 
  
$$ H_0: {\sigma_1}^2 = {\sigma_2}^2 \text{  and  } H_1: {\sigma_1}^2 \ne {\sigma_2}^2 $$

Test statistic:

$$ F = \frac{\text{larger } s^2}{\text{smaller } s^2} \sim F_{n_{larger}-1, n_{smaller}-1} $$

Reject $H_0$ if $F_{obs} > F_{n_{larger}-1, n_{smaller}-1, \frac{\alpha}{2}}$.

> R: Use `var.test` to perform an f-test.

```
var.test(Col1, Col2, alternative = "two.sided", conf.level =0.95)
```

Analysis of 2 Dependent (Paired) Quantitative Samples
===

Each individual in the 1st group is paired/matched to an individual in the 2nd group. Samples must be the same size ($n_1 = n_2$).

Paired t-test
----

Take the difference of each pair and then perform a single sample t-test.

### Conditions required for a paired t-test

* two samples are paired 
* the differences are normally distributed (compute differences and use QQ normal plot)

The test statistic and sampling distribution:

$$ t = \frac{\bar{X}_d - \mu_d}{s_d / \sqrt{n}} \sim t_{n-1} $$

> NB: $d$ is for difference. $\mu_d = 0$. $\bar{X}_d$ is the mean of the differences.

Analysis of 2 Qualitative Samples
===

Testing for the equality of two population proportions from two samples.

2 sample Z-test of proportion
----------

For two independent samples of qualitative data. 

$H_0: p_1 = p_2$

### Conditions required for a 2 sample Z-test of proportions

Sample size must be large enough for the normal approximation to be reasonable.

* $n_1\hat{p}_1 \ge 5$
* $n_1(1-\hat{p}_1) \ge 5$
* $n_2\hat{p}_2 \ge 5$
* $n_2(1-\hat{p}_2) \ge 5$

Test statistic and sampling distribution:

$$ Z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{\hat{p}(1-\hat{p})(\frac{1}{n_1}+\frac{1}{n_2})}} \sim N(0,1) $$

where $\hat{p}$ is the pooled sample proportion and is given by:

$$ \hat{p} = \frac{\text{count of successes in both samples combined}}{\text{count of observations in both samples}} $$

<script type="flashcard">
Q>>> What is the correct test, test statistic and sampling distribution for 2 independent samples of qualitative data? <<<
A>>> 2 sample Z-test of proportion. 

$$ Z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{\hat{p}(1-\hat{p})(\frac{1}{n_1}+\frac{1}{n_2})}} \sim N(0,1) $$ <<<
</script>

### Using R

    prop.test(c(x1,x2), c(n1,n2), alternative="two.sided", correct= F)

where:

* x1, x2 are the number of successes
* n1, n2 are the sample sizes
* alternative is "two.sided" or "less" or "greater"


<img src="img/summarySTA401.png" alt="summary"/>