[Home](Home.html)

[Polynomial division](http://www.maplesoft.com/support/help/Maple/view.aspx?path=Task/QuoAndRemOfPolynomialDivision)

Useful functions
---

`evalf(x)` - Produce a decimal approximation of a value.

`sqrt(x)`

`exp(x)` - `e^x`

`%` - the last expression

`Area := Pi*r^2;` - expression definition

`subs(r=5,Area);` - expression application

`Area2 := r -> Pi * r^2` - function definition

`Area2(5);` - function application

`eqn := Pi*r^2 = 80;` - equation definition

`solve(eqn,r);` - solve equation

`fsolve(eqn,r);` - solve numerically (to decimal approximation)

`fsolve(eqn,r=-1..10)` - solve in the range -1..10

`expand((x+1)^2)` - `x^2 + 2x + 1`

`factor(x^2 + 2x + 1)` - `(x+1)^2`

`diff(x^2,x)` - differentiate an expression (with respect to x)

`diff(x^2, x$2)` - 2nd derivative (or higher)

`D(x->x^2)(x)` - differentiate a function (with respect to x)

`(D@@2)(f)` - differentiate a function twice

NOTE: A suffix of @@n runs any command n times.
e.g.

    f:= x-> 2x
    (f@@2)(3) = 12

`implicitdiff(x^2 + y^2 = 1,x,y) = -x/y` - Differentiate equations (not functions)

`isolate(2x+y=60,y)` - Rearrange an equation to isolate a variable.

`unapply(x^2,x)` - Convert an expression into a function.

<script type="flashcard">
Q>>> (Maple) What is the maple function to find the derivative of an expression? <<<
A>>> `diff`

`diff(x^2,x)` <<<
Q>>> (Maple) What is the maple function to find the derivative of a function? <<<
A>>> `D`

`D(x -> x^2)(x)` <<<
Q>>> (Maple) What is the maple syntax for the 2nd derivative of $$ x^2 $$? <<<
A>>> `diff(x^2, x$2)` <<<
</script>

Plotting Functions
---

Use `plot`.

    plot(x->x^2)
    plot([f(x), g(x)], x = -2 .. 2, y = 0 .. 30, color = [green, red])

When plotting multiple functions without specifying colours, Maple uses the sequence: `red, blue, green`.

Anonymous functions can be plotted, but they have to be applied to be able to specify a range.

    plot([(x->x^2)(x),(x->(x-1)^2)(x)], x=-2..2)

### Plotting Implicit Functions

    with(plots, implicitplot)
    implicitplot(x^2 + y^2 = 1, x = -5 .. 5, y = -5 .. 5)

Taking Limits
----

Similar to plotting but use the `limit` function. Set x = the value approached by x.

    limit((x-> x^3 - 8)(x), x=2)

<script type="flashcard">
Q>>> (Maple) How would find the $$ \lim_{x \to 2} x^3 - 8 $$? <<<
A>>> `limit((x -> x^3 - 8)(x), x = 2)` <<<
</script>

Animation
----

First load the `plots` package `with(plots);`.

    animate((proc (x) options operator, arrow; k*sin(x) end proc)(x), x = -10 .. 20, k = 1 .. 4)


<script>
Q>>> (Maple) What is the tool to execute selected expressions? <<<
A>>> The `!` button <<<

Q>>> (Maple) What is the tool to execute all expressions in a document? <<<
A>>> The `!!!` button <<<

Q>>> (Maple) How does one enter a symbol? <<<
A>>> Select the symbol from the palette or start typing its name then press ESC

e.g. `pi` ESC or `sqrt` ESC or `limit` ESC <<<

Q>>> (Maple) How do you grab a previous expression? <<<
A>>> Ctrl+L then the expression label (#) at RHS <<<

Q>>>(Maple) How do you assign an expression to an identifier? <<<
A>>> Use `:=` i.e. `linear := x^2 + 5` <<<
</script>
