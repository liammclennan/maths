---
output:
  html_document:
    toc: true
---

Linear Systems
=====

[Home](Home.html)

[Matrices](Matrices.html)

[Vectors](Vectors.html)

Equations consisting of terms that are products. No radicals or exponents.

$ax + by + c = 0$ is a linear equation in two variables.

$ax + by + cz + d = 0$ is a linear equation in three variables. This is a plane in 3 dimensions (i.e. not a line).

A **linear system** is a collection of linear equations (understood to occur simultaneously).

A linear system of two equations with two variables can be solved to the point of intersection of two straight lines.

A **matrix** is a rectangle of numbers.

The **matrix of coefficients** ($A$) for the system:

$$3x - 4y=3$$
$$4y + 2z = -1$$
$$-x+5y-5z=6$$

is:

$$ \left( \begin{array}{ccc}
3 & -4 & 0 \\
0 & 4 & 2 \\
-1 & 5 & -5 \end{array} \right)$$

The **column of constants** is:

$$
\left( \begin{array}{c}
3 \\
-1 \\
6 \end{array} \right)
$$

The augmented matrix is:

$$ \left( \begin{array}{cccc}
3 & -4 & 0 & 3 \\
0 & 4 & 2 & -1 \\
-1 & 5 & -5 & 6 \end{array} \right)$$

A matrix with $m$ rows and $n$ columns is called a $m$ x $n$ matrix.  The (i,j)th entry of a matrix is the number in the ith row and jth column.

> NB. Matrices are 1 indexed, and in the opposite order to cartesian coordinates.

**Leading entry / pivot**  The leading entry (also called pivot) of a row, is the first nonzero entry in the row (looking left to right).

**Diagonal of a (square) matrix)**. A diagonal of a square matrix, are the numbers on the diagonal from top left to bottom right.

**Triangular matrix**. An upper triangular matrix is a square matrix so that all numbers below the diagonal are zero. An lower triangular matrix is a square matrix so that all numbers above the diagonal are zero.

**Diagonal matrix**. A Diagonal matrix is a square matrix which has non-zero entries
only on its diagonal. Note: zeroes are allowed on the diagonal.

**Row echelon form**. A matrix is in row echelon form if

* rows of zeroes are at the bottom, and
* leading entries in lower rows are to the right of leading entries in the above rows.

Solve from the bottom up.

**Reduced row echelon form**. A matrix is in reduced row echelon form (RRE) if

* rows of zeroes are at the bottom,
* leading entries are all 1,
* leading entries in lower rows are to the right (ie there are 0s below all leading entries), and
* there are 0s above all leading entries.

**Submatrix** - given a matrix $A$, the $( i th, j th)$ submatrix, $A_{ij}$ is the matrix obtained from $A$ by deleting the i th row, and j th column.

Row Operations
----

#### Addition / Subtraction

Add or subtract multiples of one row to/from another. E.g. $R2 := R2 - 3R1$

#### Multiply a row by a non-zero constant

#### Swap rows E.g. $R3<->R4$.

Gaussian Elemination
-----

A guaranteed way to produce row echelon form.

Suppose that by using the algorithm the first k-1 rows are already in the right form (row echelon form) [you start the algorithm with k = 1]

* By swapping rows if necessary, make sure the left most nonzero entry in rows k,k+1,... is in the kth row. If all these rows are zero then you are finished.
* Let a kl be the leading entry of the kth row (ie it is in column l). Then divide the kth row by a kl .
* For each row (call it row i) below the kth row, with entry a il below the leading entry of the kth row,
subtract a il times row k from row i.
* (If you would like to get reduced row echelon form, then also for each row (call it row i) above the kth row, with entry a il above the leading entry of the kth row, subtract a il times row k from row i.) The algorithm finishes when you have only rows of zeros left, or you run out of rows.

### Free variable

Variable without an equation. E.g. in a system of two functions with 3 variables one of them is a free variable (could be any). In row echelon form, variables whose column does not have a leading entry are free variables.

### Inconsistent linear system

System having no solution. Corresponds to a geometric system with no intersection. In RRE form may look like a row (0 0 1) (i.e. 0=1).

With Maple
------

Useful packages:

    with(plots); # for implicitplot
    with(LinearAlgebra);

### Solve a linear system

    sys := {x+2*y = 5, 3*x-y = 1}
    implicitplot(sys, x = -5 .. 5, y = -5 .. 5)
    solve(sys,{x,y})

### Guassian Elemination and Backwards Substitution

    A := <<1, 2, 3>|<1, 4, 6>|<2, -3, -5>>
    b := <9, 1, 0>
    aug := <A|b>
    GaussianElimination(aug)
    BackwardSubstitute(C)
    ReducedRowEchelonForm(aug)
