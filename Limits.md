[Calculus](Calculus.html)

Limits
===

The value of a function as its argument nears a certain value.

### One-sided Limit

Limits can be one sided. One-sided limits approach from below:

<img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E-%7D%20f%28x%29"\>

or from above:

<img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E+%7D%20f%28x%29"\>

<script>
Q>>> Does <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E-%7D%20f%28x%29"\> mean the limit from above or from below?  <<<
A>>> <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E-%7D%20f%28x%29"\> means the limit from below. <<<
Q>>> Does <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E+%7D%20f%28x%29"\> mean the limit from above or from below?  <<<
A>>> <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E+%7D%20f%28x%29"\> means the limit from above. <<<
</script>

### Two-sided Limit

if
<img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E+%7D%20f%28x%29"\> = <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%5E+%7D%20f%28x%29"\> then <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%5Cto0%7D%20f%28x%29" /> is the two-sided limits. Otherwise the 2-sided limit does not exist.

Calculating Limits
---

### Subbing

To find <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%20%5Cto%20a%7D%20f%28x%29" /> sub in values increasingly closer to `a`. If `f(a)` is defined then that is the limit. For continuous functions then `f(a)` is always defined. Indeed, the definition of a continuous function is <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx%20%5Cto%20a%7D%20f%28x%29%20%3D%20f%28a%29"/>.

### Using 1/x

For limits `x->inf` we can use the fact that <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx-%3E%5Cinfty%7D%5Cfrac%7B1%7D%7Bx%7D%20%3D%200"/>. By rearranging the expression to include `1/x` we introduce `0`s that help to simplify.

#### Finding limits of rational expressions using 1/x

The proceedure to find limits of rational expressions by using <img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx-%3E%5Cinfty%7D%5Cfrac%7B1%7D%7Bx%7D%20%3D%200"/> is:

* divide numerator and denominator by the largest power of x in the denominator.
* Rewrite in terms of `1/x`
* Substitute `1/x -> 0`

NOTE: **only works for limits to infinity**

### Using Dominant Function Method

Useful for finding the **limit to infinity** of rational expressions. When taking the limits of sums or differences we can ignore all but the dominant function. The dominant function is the one that changes quickest as the limit is approached. Much like summing O complexities.

Limits of 1/x
---

`f(x) = 1/x` provides an example of a number of different limits. We have x->0 from both sides,  x->inf and x->-inf

<img src="img/1onX.png"/>

<script>
Q>>> $$ \lim_{x->0^-}\frac{1}{x} = ? $$ <<<
A>>> $$ \lim_{x->0^-}\frac{1}{x} = -\infty $$ <<<
Q>>> $$ \lim_{x->0^+}\frac{1}{x} = ? $$ <<<
A>>> $$ \lim_{x->0^+}\frac{1}{x} = \infty $$ <<<
</script>

Operations on Limits
---

`+, -, /, *` and composition (for continuous functions) are all preserved for limits. This means that a limit can be split into parts and calculated separately. e.g.

<img src="http://latex.codecogs.com/gif.latex?%5Clim_%7Bx-%3Ea%7D%5Cfrac%7Bf%28x%29%7D%7Bg%28x%29%7D%20%3D%20%5Cfrac%7B%5Clim_%7Bx-%3Ea%7Df%28x%29%7D%7B%5Clim_%7Bx-%3Ea%7Dg%28x%29%7D"/>

L'Hôpital's rule
---

Given a ratio of two functions `f(x)/g(x)` if it is an `indeterminate form`, and `f(x)` and `g(x)` are differentiable then:

    f(x) / g(x) = f'(x) / g'(x)

This can be used to simplify the evaluation of the limit.

NOTE: Indeterminate forms are `(y/0)` and `(+-infty/+-infty)`. To check try substitution.

NOTE: The process can be applied repeatedly.
