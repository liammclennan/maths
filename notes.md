<style>
body {  text-align:left; }
span.LaTeX > table {
  background-color: white !important;
  padding: 0px;
}
span.LaTeX > span {
  background-color: white !important;
  padding: 0px;
}
p {margin-top:0px; margin-bottom:2px}
table {border-top: 1px solid black;}

</style>

_**1-Sample Hypothesis Tests**_

<table><tr><th>
General Z
</th><td>
$Z = \frac{x - \mu}{\sigma}$
</td><td>
Random sample | Population is normal
</td></tr></table>

<table><tr><th>
1-Sample Z-test
</th><td>
$Z = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0,1)$</td><td>
Random sample | Population is normal | $n > 30$ | $\sigma$ is known
</td></tr></table>

<table><tr><th>
1-Sample T-test ($H_0: \bar{X} = \mu$)
</th><td>$t = \frac{\bar{X} - \mu_0}{\frac{S}{\sqrt{n}}} \sim t_{n-1}$</td><td>
Random sample | Population is normal
</td></tr></table>

<table><tr><th>1-Sample test of proportion <br/>($H_0:\hat{p} = p$)</th><td>$Z = \frac{\hat{p} - p}{\sqrt{\frac{p(1-p)}{n}}} \sim N(0,1)$</td><td>
Random sample | $np>5$ $n(1-p)>5$
</td></tr></table>

_**1-Sample Confidence Intervals**_

<table><tr><th>When $\sigma$ is known</th><td>$\bar{x} \pm Z^* \frac{\sigma}{\sqrt{n}}$ where $Z^*$ is $\alpha/2$ of $t_{9999}$</td>
<td>$\sigma$ is known | $n>30$ | $\bar{x}$ is normal | symetrical unimodal | SRS | no outliers</td></tr></table>

<table><tr><th>When $\sigma$ is unknown</th>
<td>$$\bar{x} \pm {t^*}_{n-1} \frac{s}{\sqrt{n}}$$</td>
<td>$n>30$ | $\bar{x}$ is normal | symetrical unimodal | SRS | no outliers</td></tr></table>

<table><tr><th>Population proportions</th>
<td>$\hat{p} \pm {z^*} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$</td>
<td>$n\hat{p} >5$ and $n(1-\hat{p}) > 5$</td></tr></table>

<table><tr><th>Sample Size for Required Margin of Error (Quantitative Data)</th>
<td>$$ n = (\frac{z^*\sigma}{m})^2 $$</td>
</tr><tr><th>Sample Size for Required Margin of Error (Qualitative Data)</th>
<td>$$ n = (\frac{z^*}{m})^2 p(1-p) $$</td>
</tr></table>

_**2-Sample Hypothesis Tests**_

<table><tr><th>Welch 2-sample t-test $H_0: \mu_1 = \mu_2$</th>
<td>$t = \frac{\bar{X}_1-\bar{X}_2-(\mu_1-\mu_2)}{\sqrt{\frac{s^2_1}{n_1} + \frac{s^2_2}{n_2}}} \sim t_{df}$</td>
<td>tests population means | independent groups | normal populations</td></tr></table>

<table><tr><th>Pooled t-test $H_0: \mu_1 = \mu_2$</th>
<td>crazy town</td>
<td>tests population means | independent groups | normal populations | *requires equal variance*</td></tr></table>

<table><tr><th>F-test of variance ($H_0: {\sigma_1}^2 = {\sigma_2}^2$ and $H_1: {\sigma_1}^2 \ne {\sigma_2}^2)$</th>
<td>$F = \frac{larger \: s^2}{smaller \: s^2} \sim F_{n_{larger}-1, n_{smaller}-1}$</td>
<td>Reject $H_0$ if $F_{obs} > F_{n_{larger}-1, n_{smaller}-1, \frac{\alpha}{2}}$</td></tr></table>

<table><tr><th>Paired t-test $H_0: \mu_1 = \mu_2$</th>
<td>$t = \frac{\bar{X}_d - \mu_d}{s_d / \sqrt{n}} \sim t_{n-1}$</td>
<td>$n_1 = n_2$ | $\bar{X}_d$ is the mean of the pair differences | $\mu_d=0$ | differences are normal</td></tr></table>

<table><tr><th>2-Sample Z-test of proportions ($H_0: p_1 = p_2$)</th>
<td>$Z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{\hat{p}(1-\hat{p})(\frac{1}{n_1}+\frac{1}{n_2})}} \sim N(0,1)$</td>
<td>$n_1\hat{p}_1 \ge 5$ | $n_1(1-\hat{p}_1) \ge 5$ | $n_2\hat{p}_2 \ge 5$ | $n_2(1-\hat{p}_2) \ge 5$ | $\hat{p}$ is $\frac{total \: successes}{total \: observations}$
</td></tr></table>

_**n-Sample Hypothesis Tests**_

<table><tr><th>ANOVA ($H_0: \mu_1 = \mu_2 = \mu_3 .. = \mu_k$)</th>
<td></td>
<td>Random errors mean = 0 | RE have same variance  | RE are normally distributed | Are independent</td></tr></table>

<table><tr><th>Tukey's method for multiple comparisons</th>
<td></td>
<td>0 in the CI indicates that the means could be the same</td></tr></table>

<table><tr><th>Chi Square Goodness of Fit (For qualitative data with counts of categories. Tests observed against expected counts) $H_0: obs \: fit \: pattern$</th>
<td>$\chi^2 = \sum \frac{observed^2}{expected} -N \sim \chi^2_{df}$</td>
<td>$N =$ total count across all categories  | $df =$ # categories - 1 | all category counts > 0 | < 20% of expected counts < 5 | each trial falls into exactly one category</td></tr></table>

<table><tr><th>Chi Square Test of independence $H_0: variables \: are \: independent$</th>
<td>$\chi^2 = \sum \frac{observed^2}{expected} -N \sim \chi^2_{(r-1) * (c-1),\alpha}$</td>
<td>Values are *col total* * *row total* / *total*</td></tr></table>

_**Regression Hypothesis Tests**_

<table><tr><th>Inferring Population Correlation $H_0: \rho = 0$ $H_0: \rho \ne 0$</th>
<td>$t = \frac{r - \rho}{\sqrt{\frac{1-r^2}{n-2}}} \sim t_{n-2}$</td>
<td></td></tr></table>

<table><tr><th>Testing regression significance ($H_0: \beta = \beta_0$ usually $H_0: \beta = 0$)</th>
<td>$t = \frac{b - \beta}{SE_b} \sim t_{n-2}$</td>
<td></td></tr></table>
