Hypothesis Testing
===

A type of inference. Asses the evidence provided by a sample about some claim concerning a population parameter. Eg. If a player makes 8 of 20 free throws does that indicate that their claim of making 75% of free throws is false? (Answer: yes. The probability of making 8 of 20 given a 75% rate is 0.0009 (p-value), which is less than 0.05)

Given information about a population and a sample we may want to show if the difference is statistically significant.

<script>
Q>>> Hypothesis testing (tests of significance) is a technique to ... <<<
A>>> Infer from a sample statistic if that statistic matches the population, within a specified level of significance. <<<
</script>

Summary of Steps in Hypothesis Testing
---

1. Write the null and alternative hypothesis.

1. State the level of significance (0.05 by default) (written $\alpha$)

1. State the test statistic and its sampling distribution

1. Find the rejection criterion

1. Calculate the p-value or test statistic

1. Decision and conclusion

### The Null Hypothesis ($H_0$)

The null hypothesis is the 'no change' or 'no effect' hypothesis. For this hypothesis testing the null hypothesis is that the population and sample are the same.

### Alternative Hypothesis ($H_a$)

The hypothesis that this is a change. Indicated by showing that the observed values are sufficiently unlikely (less than the level of significance) under the null hypothesis.

P-values
---

The probability (assuming $H_0$) that the test statistic equals or is more extreme than the observed value. ie the probability of the observed result under the null hypothesis.

Critical Values
---

Approximate P-values using a test statistic and critical values from a table.

Types of Errors
----

### Type 1 Error

$H_0$ is true, but we reject it. I.e. we claim a statistically significant effect when there isn't one. 

> Convicting an innocent person

### Type 2 Error

$H_0$ is false, ($H_a$ is true) but we do not reject $H_0$. I.e. there is a statistically significant effect, but we do not claim it.

> Releasing a guilty person

Power
----

Probability of correctly rejecting $H_0$. Probability of rejecting H_0|it is false.
