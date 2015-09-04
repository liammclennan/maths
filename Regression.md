[Statistics](Statistics.html)

Regression
=======

**Bivariate / paired data** values of two different variables that are obtained from the same population. Written as *ordered pairs* $(a,b)$.

**Response / dependent / y variable** is the variable we try to predict.

**Explanatory / predictor / independent / x variable** is the variable used to predict.

Describing the relationship between two variables
-----

**Nature** is a description of the relationship.

**Strength** is a description of how well the data matches the pattern.

**Outliers** are data that don't match the pattern.

**Correlation coefficient ($r$)** measures the direction and strength of a linear relationship between two quantitative variables from a sample. $[-1,1]$

### Using R Commander

    Statistics-> Summaries -> Correlation matrix

or with R (correlation between pairs from two vectors):

    cor(duration, waiting)

> NOTE: correlation is not robust. It is strongly affected by outliers.

### Infering population correlation from a sample

This is a test to see if the sample correlation coefficient says anything significant about the population. Large (absolute) values or $r$ and large sample sizes contribute to a significant result.

$r$ is the linear correlation coefficient of the sample.

$\rho$ (rho) is the linear correlation coefficient of the population.

Use a hypothesis test. Hypotheses are:

$$ H_0: \rho = 0 $$
$$ H_a: \rho \ne 0 $$

Test statistic is:

$$ t = \frac{r - \rho}{\sqrt{\frac{1-r^2}{n-2}}} \sim t_{n-2} $$

> NOTE: There are $n-2$ degrees of freedom

### Using R Commander

    Statistics->Summaries->Correlation test

### Assumptions

Both variables should be normally distributed. Check with qq normal plots.

Line of best fit
----

An estimate of the best linear relationship between two variables. Useful for predicting other points.

Least Squares Regression
-----

Minimise the squares of the vertical distances between the points and the line.

$$ \hat{y} = a + bx $$

$a$ and $b$ are called the **regression coefficients**.

### Calculate a linear regression with R Commander

Statistics->Fit models -> Linear regression

or with R

    m <- lm(frame$column ~ frame$othercolumn)
    summary(m)

The output includes t values and p values that describe the probability of the linear relationship being significant.

### Coefficient of Determination ($R^2$)

The percentage of total variability in the
response (y) that is explained by the least squares regression line.

R lists it as "multiple R squared".

### Residuals

The vertical distance (upwards) from the regression line to each point is called **residuals** because it represents the residual variation.

$$ residual = observed y - predicted y $$
$$ \hat{y} - y $$

### Linear Regression Assumptions

For a reasonable model we expect the random errors (residuals) to:

* have a zero mean

The mean of the residuals is 0 automatically (if
there is an intercept).

* be normally distributed

Same check as ANOVA. In R cmder Models->Graphs->Basic Diagnostic plots. Check for normal distribution of random errors using the QQ normal plot or the residuals (top right).

* have equal variance

Check the plot of residuals against fitted values.

* be independent of each other

Look for a random scatter in the Residuals vs fitted graph and consider how the data was collected and argue for or against it.

### Hypothesis test of slope

To test if x can be used to predict y, ie is there a linear relationship, ie is the slope $\ne 0$?

$b$ is the sample slope. $\beta$ is the population slope.

Hypotheses:

$$ H_0: \beta = \beta_0 $$
$$ H_a: \beta \ne \beta_0 $$

Test statistic:

$$ t = \frac{b - \beta}{SE_b} \sim t_{n-2} $$

Get $b$ and $SE_b$ from R linear model.

### Slope confidence interval

$$ b \pm { t^* }_{n-2}SE_b $$

Gives plausible values for the slope. If $0$ is not in the interval it suggests a significant linear relationship.

### Hypothesis test of intercept

To test if the intercept equals a certain value

Hypotheses:

$$ H_0: \alpha = \alpha_0 $$
$$ H_a: \alpha \ne \alpha_0 $$

Test statistic:

$$ t = \frac{a - \alpha}{SE_a} \sim t_{n-2} $$

### Intercept confidence interval

$$ a \pm { t^* }_{n-2}SE_a $$

Gives plausible values for the intercept. If $0$ is not in the interval it suggests a significantly non-zero intercept.

General Test of the Model
----

Hypotheses:

$H_0:$ data fit the model
$H_a:$ data do not fit the model

Test statistic:

    the ratio of the variance of the model and the variance of the residuals / error.

$$ F = \frac{MS(model)}{MSE} = \frac{R^2}{(1-R^2)/(n-2)} \sim F_{1,n-2} $$

$MSE$ is "residual standard error" in R output. $F$ value is shown as "F-statistic".
