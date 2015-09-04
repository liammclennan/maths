Differential Equations
=========

Equation containing an unknown function and one or more of its derivatives. E.g.

$$ \frac{dy}{dx} = 3x^2 $$

$y$ is the unknown function.

Used in modelling when we want to predict future behaviour on the basis of how current values change.

A differential equation relates a function to its derivative.

Order
----

A first order differential equations involves only first order derivatives.

Ordinary
-------

An ordinary differential equation is one where the unknown function is a function of one variable only.

Solution
----

To `solve` a differential equation is to identify the unknown function. For

$$ y' = xy $$

it is *understood* that $y$ is an unknown function of $x$. $f$ is a solution to the equation if:

$$ f'(x) = xf(x) $$

for all $x$ in some interval.

### Solve on TI-nspire

`deSolve(y'=y^2,x,y)`

or as an initial value problem:

`deSolve(y'=y^2 and y(0)=100,x,y)`

### Solve initial value problems

1. Solve the differential equation to an implicit or explicit function.

1. Substitute the initial values and solve for the unknown value.

Separable Differential Equations
---------------------

Differential equations that can be expressed as a product of a function of $x$ and a function of $y$ e.g.

$$ \frac{dy}{dx} = 2x\sqrt{y} $$

to solve

1. Multiply both sides by the inverse of the function of $y$

$$ \frac{1}{\sqrt{y}} \frac{dy}{dx} = 2x $$

1. Integrate both sides with respect to $x$

$$ \int \frac{1}{\sqrt{y}} \frac{dy}{dx} dx = \int 2x \: dx $$
$$ 2y^{1/2} = x^2 + c $$
$$ y = (\frac{x^2 + c}{2})^2 $$

Linear differential equations
-----------------------------

A first order linear differential equation that can be written in the (standard) form:

$$ \frac{dy}{dx} + P(x)y = Q(x) $$

where $P(x)$ is some function of $x$, $Q(x)$ is another function of $x$.

The solution is:

$$ y(x) = \frac{1}{v(x)}[\int v(x)Q(x)dx + c] $$

where $v(x) = e^{\int P(x) dx}$

### To solve a first order linear differential equation

> Multiply both sides by the integrating factor $v(x) = e^{\int P(x) dx}$ and integrate both sides.

Method 2:
---

1. Multiply both sides by the integrating factor, and arrange into the form:

$$ y' g + g' y = q $$

2. Apply the reverse product rule:

$$ f'g + g'f = (gf)' $$

therefore:

$$ (gf)' = q $$

Models for population growth
-----

### The law of natural growth

The population grows at a rate proportional to the size of the population.

$$ \frac{dP}{dt} = kP $$

This is a separable differential equation which solves to:

$$ P(t) = P_0 e^{kt} $$

$P_0$ is the initial population.

### The Logistic Model

A model for population growth that accounts for the carrying capactiy of the system:

$$ \frac{dP}{dt} = kP(1 - \frac{P}{M}) $$

> $M$ is the carrying capacity.

When P is small (relative to M) we have approximately *the law of natural growth*.

The limit (P -> M) of $1 - \frac{P}{M}$ is 0. Therefore, as the population approaches the carrying capactiy $\frac{dP}{dt}$ -> $0$.

Heating and Cooling
-----

From Newton's law of heating and cooling:

$$ \mbox{rate of temperature change} = \mbox{constant} * \mbox{temperature difference} $$

i.e. Rate of change of temperature is proportional to the temperature difference.

$$ \frac{dK}{dt} = -k(T - T_s) $$

$k$ is the *heat transfer coefficient* and relates to thermal conductivity between the two bodies.

$T$ is the temperature of the object heating or cooling, and $T_s$ is the temperature of the surroundings.

The equation above is a separable differential equasion with solution (for $T$):

$$ T(t) = Ae^{-kt} + T_s $$

Concentrations (Mixing problems)
------

The equation that relates a quantity being mixed to its rate of change is informally:

$$ \mbox{change in quantity} = \mbox{rate in} - \mbox{rate out} $$

For a system with an even flow in and out, and perfect mixing this is:

$$ \frac{dx}{dt} = rc - \frac{rx}{V} $$

$r$ is the flow rate, $c$ is the incoming concentration, and $\frac{x}{V}$ is the outgoing concentration.

The equation above solves to (for $x$):

$$ x(t) = V(Ae^{-rt} + c) $$

Interest
------

Where $A(t)$ is the balance of an account at time $t$.

$$ \frac{dA}{dt} = rA $$

Where $r$ is the interest rate (for 5% loan the rate is 0.05). I.e. the rate of change of the balance of the account is proportional to the interest rate.

If there are other regular changes to the balance (debits or credits) then the rate of change of the balance is the difference between the change due to interest and the change due to other scheduled transfers:

$$ \frac{dA}{dt} = rA - S $$

Where $S$ is a regular debit or credit.
