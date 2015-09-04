Descriptive statistics
======

Population
---

The full set of measurements.

Sample
---

A subset of the population.

Variable
----

A characteristic of an item in the sample or population.

Statistic
---

Numerical description of a sample characteristic. e.g. mean of a sample.

Parameter
----

Numerical description of a population characteristic. e.g. mean of a population.

Data Classification
----

Qualitative or Quantitative

Qualitative can be **nominal** or **ordinal**. Ordinal means the number shows the order.

Quantitative can be interval scale (like Celcius) or ratio scale (has a meaningful zero, like Kelvin).

Discrete or Continuous.

Displaying Data
----

Graphical or tabular (e.g. frequency table shows counts of category frequencies).

For qualitative data use a pie chart or bar chart.

For quantitative data use a histogram or box plot. Histogram is only good for continuous data.

### Bivariate Data

Use a scatterplot. Shows the relationship between two quantitative variables. Put the independent variable on the x axis and the dependent variable on the y axis.

Measures of central location
----

### Mean

$$ \bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i $$

### Median

The middle value. For an odd-numbered collection take middle value. For an even numbered collection take the average of the two middle values.

### Mode

The value that occurs the most times. Important for qualitative data.

### Standard Deviation

A measure of dispersion of a set of data values. Represented by lower case sigma (σ) for populations and s for samples.

The square root of the sum of the squared difference of each item from the mean divided by `n` (for population) or `n-1` (for sample).

http://en.wikipedia.org/wiki/Standard_deviation#Basic_examples

### Sample Variance

Written $s^2$. The sum or the squared differences of each item from the mean, divided by `n` (for population) or `n-1` (for sample). The standard deviation squared.

$$ s^2 = \frac{1}{n-1}\sum_{i=1}^n (x_i - \bar{x})^2 $$

<script>
Q>>> What is the formula for sample variance? <<<
A>>> SampleVariance $$ = s^2 = \frac{1}{n-1}\sum_{i=1}^n (x_i - \bar{x})^2 $$ <<<
</script>

### Standard error of the mean

A convention that informs the reader how variable the observed mean is as an estimate of the true mean.

$$ SE_{\bar{x}} = \frac{s}{\sqrt{n}} $$

<script>
Q>>> What is the equasion for `Standard error of the mean`? <<<
A>>> $$ SE_{\bar{x}} = \frac{s}{\sqrt{n}} $$ <<<
</script>

### Inter quartile range

The 75th percentile - the 25th percentile.

    IQR = Q_{3} - Q_{1}

### Range

Largest observation - smallest observation.

### Coefficient of variation

CV. In probability theory and statistics, the coefficient of variation (CV) is a standardized measure of dispersion of a probability distribution or frequency distribution. It is defined as the ratio of the standard deviation to the mean.

$$ \frac{s}{\bar{x}} $$

<script>
Q>>> What is the equasion for `Coefficient of variation`? <<<
A>>> $$ CV = \frac{s}{\bar{x}} $$.

The coefficient of variation (CV) is a standardized measure of dispersion of a probability distribution or frequency distribution. It is defined as the ratio of the standard deviation to the mean. <<<
</script>

Skewness
-----

Data is skewed to the extent that the mean and median differ. Non-skewed data is called **symmetric**.

### Skewed to the right

The mean is greater than the median. The  bulge is on the left.

<script>
Q>>> The mean of a sample is 3. The median is 2. What is the skewness? <<<
A>>> The mean is greater than the median so the data is right skewed. <<<
Q>>> The mean of a sample is 7. The median is 9. What is the skewness? <<<
A>>> The mean is less than the median so the data is left skewed. <<<
</script>

### Skewed to the left

The mean < median. The bulge is on the right.
