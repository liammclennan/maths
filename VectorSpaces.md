Vector Spaces
======

[Vectors](Vectors.html)

A set of elements satisfying the vector axioms for *vector addition* and *scalar multiplication*.

Vector Addition axioms
-------

* If $u$ and $v$ $\in V$ then $(u+v) \in V$. (closed under addition)
* $u + v = v + u$ (commutativity)
* $u + (v + w) = (u + v) + w$ (associativity)
* There is a zero vector such that $u+0 = u$ for all $u \in V$.
* For each $u \in V$ there is a (negative) $-u$ such that $u + (-u) = 0$. Note that $-u$ is not necessarilly $(-1)u$.

Scalar multiplication axioms
------

* If $k$ is a scalar then $ku \in V$. (closed under multiplication)
* $k(u + v) = ku + kv$ (distributive law)
* $(k + m)u = ku + mu$ (distributive law)
* $k(mu) = (km)u$
* $1u = u$

Subspaces
========

A subspace is a subset of another subspace that still meets all the requirements to be a vector space.

For vector spaces ($VV$) over $R$, the subset $W$ is a subspace of $V$ if forall $u,v \in W, c \in R$:

1. $u + v \in W$ (closed under addition)
1. $cu \in W$ (closed under multiplication)

Finite Dimensional Vector Space
----

If it is possible to span a vector space $V$ over $\mathbb{R}$ using a finite set of
vectors, then we say $V$ is a *finite dimensional vector space*. E.g. $R^3$ is an infinite vector space with a finite basis.

$P_\infty$ is an infinite vector space with an infinite basis.

Linear Independence
------

The vectors $v_1,...,v_r$ are linearly independent if none of them can be written as a linear combination of the others.

$v_1,...,v_r$ are linearly dependent if there exists constants such that $c_1v_1,...,c_rv_r = 0$.

In matrix form this is

$$ (v_1 ... v_r) \left( \begin{array}{c}
c_1 \\
... \\
c_r \end{array} \right) = \left( \begin{array}{c}
0 \\
... \\
0 \end{array} \right) $$

If the matrix $(v_1 ... v_r)$ (each vector is a row) has $det = 0$ then the vectors are linearly dependent. The matrix has infinite solutions, hence the linear dependence. A single solution ($det \ne 0$) indicates a solution where all coefficients are 0, hence linearly independent.

If there are more vectors than elements in the vectors then they are not linearly independent.

Dimension
-----

The *dimension* of a vector space is the number of vectors in its basis.
