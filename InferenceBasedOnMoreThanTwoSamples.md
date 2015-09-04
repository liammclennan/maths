[Home](Home.html) -> [Statistics](Statistics.html) -> [Inference](Inference.html)

Inference Based on More Than Two Samples
====

Analysis of Variance (ANOVA) (AOV)
---

Use sample data to see if the values of more than two unknown population
means are likely to be different. Using a technique that requires multiple comparisons (e.g. each pair) is tedious and prone to [type 1 errors](HypothesisTesting.html) (because of multiple comparisons - then tests at $p=0.05$ is $p=0.5$).

ANOVA determines if population means are different by looking at the

* means of the samples
* variance of the samples

#### The Null Hypothesis

The null hypothesis for ANOVA is:

$$ H_0: \mu_1 = \mu_2 = \mu_3 .. = \mu_k $$

#### The Alternative Hypothesis

Not all of the means are equal. The alternative hypothesis is non-directional.

### The F Test

The F Test is the test statistic used for ANOVA.

$$ MS = s^2 = \frac{\sum_i (x_i  -\bar{x})^2}{n-1}$$


$$ F = \frac{\text{Variation between samples}}{\text{variation within samples}} = \frac{MSG}{MSE} $$

Reject $H_0$ if $F > F_{dfG,dfE,\alpha}$

$dfG$ (numerator) is the number of groups minus 1.

$dfE$ (denominator) is the total number of samples in all groups minus the number of groups.

#### R Commander Instructions

1. Enter data in two columns. Values | Group. Use labels for the groups.

1. Statistics -> Means -> One way ANOVA

### Rough Assumption of ANOVA

* the individual samples come from
independent populations;
* these populations all have Normal
distributions; and
* the populations have the same variance. Boxplot. If smallest sd/spread > half of the largest sd/spread then OK. Or check $\frac{s_{largest}}{s_{smallest}} < 2 = s^2_{largest} < 4s^2_{smallest}$.

### Precise Assumptions of ANOVA

$i =$ group, $j=$ point.

The random errors $E_{ij}$ ($value - \mu_i$):

* Have mean of 0
* All have the same variance
* Are normally distributed
* Are independent of each other.

Check with R Commander:  Models -> Graphs -> Basic Diagnostic plots

Check residuals have same variance by checking the spread of dots in the first graph.

Check residuals are normally distrubuted by looking for straight line in residuals QQ normal plot.

### Multiple Comparisons

ANOVA provides an indication of if there exists a difference between some population means. It does not indicate which populations are different or how they differ. Do discover this we use **multiple comparisons**.

Tukey's method is based on confidence intervals for the differences between groups. 0 in the confidence interval indicates that the difference is not significantly different.

In R Commander use **Statistics->Means->One way ANOVA** with **Pairwise comparisons of means**.

Chi Square Test
=====

For qualitative data, with counts of categories, use Chi Square test.

Effectively test **observed** counts against **expected** counts.

Not reliable for small samples.

Goodness of fit
----

Comparing observed counts to expected counts.

Hypothesis is:

$$ H_0: \text{observations fit the pattern} $$
$$ H_a: \text{observations do not fit the pattern} $$

> The Chi Square test statistic is a measure of how far the observed counts are from the expected counts. The test statistic formula is:

$$ \chi^2 = \sum \frac{(observed - expected)^2}{expected} \sim \chi^2_{df} $$

or equivalently:

$$ \chi^2 = \sum \frac{observed^2}{expected} -N \sim \chi^2_{df} $$

Where $N =$ the total count across all categories.

$df =$ number of categories $- 1$.

### Assumptions of Chi Square test:

1. No **expected** count is less than one.

1. No more that 20% of the **expected** counts are $<5$.

1. The outcome of each trial falls into exactly one of the categories.

### Using R

    csq <- chisq.test(c(o1,o2,…), p=c(p1, p2, …))
    csq
    csq$expected
    csq$observed

Where `o1,o2...` are the observed counts and `p1, p2...` are the probabilities.

Test of Independence
----

Test if two categorical variables are independent. This is a special case of the goodness of fit test. Used for cross-tabulated data in contingency tables.

$$ H_0: \text{variables are independent} $$
$$ H_a: \text{variables are dependent} $$

### Steps

1. Construct contingency table. Calculate expected values from the sub-totals by:

$$ \frac{\text{row total} * \text{column total}}{\text{grand total}} $$

2. Apply test statistic

$$ \chi^2 = \sum \frac{observed^2}{expected} -N \sim \chi^2_{(r-1) * (c-1),\alpha} $$

> $df$ is rows - 1 * columns - 1.

### Using R Commander

    Statistics->Contingency table->Enter and analyse two-way table
