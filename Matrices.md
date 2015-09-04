---
output:
  html_document:
    toc: true
---

Matrices
====

[Linear Systems](LinearSystems.html)
[Vectors](vectors.html)

Transpose
------

Interchange rows and columns. $a_{ij}$ becomes $a_{ji}$.

$$ \left( \begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \end{array} \right)^T = \left( \begin{array}{cc}
1 & 4 \\
2 & 5 \\
3 & 6 \end{array} \right) $$

Addition and Subtraction
----

If we have two matrices A and B which are the same size, m  n, then we can add or subtract termwise.

Scalar Multiplication
----

If we have two matrices A and B which are the same size, m  n, then we can scalar multiply termwise.

Matrix Multiplication
----

To multiple $m * n$ by $p * q$ we must have $n=p$. The resulting matrix is $m * q$.

The multiply corresponding terms of each row of `m` by each column of `q`.

Matrix Powers
----

Defined if $m = n$ ie the matrix is square.

Zero Matrix
----

$0_{m*n}$ is the matrix such that $A + 0_{m*n} = A$. It is a matrix of all zeros and the same dimensions as the matrix it is added to.

Negative Matrix
-----

The matrix such that $A + -A = 0$, which is $-1*A$.

'One' Matrix (Identity Matrix) (I)
------

The matrix such that $A_{mn} * I = A_{mn}$. The identity matrix must be $n * n$ and is written $I_n$. It is a square matrix with ones on the top-left to bottom-right diagonal and all other numbers 0. E.g.

$$ I_n =  \left( \begin{array}{cc}
1 & 0  \\
0 & 1  \end{array} \right) $$

and

$$ A_{mn} I_n = A_{mn} $$

Differences between matrix laws and real number laws
-------

Matrix multiplication is not commutative:

$$ AB \ne BA $$

$AB = 0$ does not necessarilly imply that either $A$ or $B = 0$.

Matrix Inverse ($A^{-1}$)
------

Given a matrix $A$ , if there is a matrix $B$ such that $AB = I = BA$ then $B$ is said to be the inverse of $A$ and it is written $B = A^{-1}$. Also $A$ is said to be *invertible*.

$A^{-1}$ must be square (as must $A$).

Rules:

* The inverse matrix (if it exists) is unique.
* If $A$ and $B$ are invertible then $AB$ is invertible.

### Gauss-Jordan Method to find inverses

1. Augment $A$ with $I_n$ to get $(A|I_n)$.

1. Get the augmented matrix into reduced row echelon form.

1. If the RRE form is $(I_n|B)$ then $B$ is the inverse of $A$.

1.   If the reduced row echelon form is $(R|B)$ where $R$ has a row of zeroes then A is not invertible.

### Inverses of 2 by 2 matrices

$$ \left( \begin{array}{cc}
a & b  \\
c & d  \end{array} \right)^{-1} = \frac{1}{ad-bc} \left( \begin{array}{cc}
d & -b  \\
-c & a  \end{array} \right) $$

thus, if $ad-bc = 0$ then the matrix is not invertible. The expression $ad-bc = 0$ is called the *determinant*.

### Using Inverses

Use inverses to solve equations requiring division.

$$ 2x + y = 3 $$

$$ -5x -3y =1$$

$$ \left( \begin{array}{cc}
2 & 1  \\
-5 & -3  \end{array} \right) \left( \begin{array}{c}
x  \\
y  \end{array} \right) = \left( \begin{array}{c}
3  \\
1  \end{array} \right) $$

$$ \left( \begin{array}{c}
x  \\
y  \end{array} \right) = \left( \begin{array}{cc}
2 & 1  \\
-5 & -3  \end{array} \right)^{-1} \left( \begin{array}{c}
3  \\
1  \end{array} \right) $$

$$ = \left( \begin{array}{cc}
3 & 1  \\
-5 & -3  \end{array} \right) \left( \begin{array}{c}
3  \\
1  \end{array} \right) $$

$$ = \left( \begin{array}{c}
10  \\
-17  \end{array} \right) $$

If the matrix has no inverse then the system has no solutions, or infinite solutions.

Singular Matrix
------

A square matrix that is not invertible is called `singular` or `degenerate`.

Determinants
--------

A single number calculated from a square matrix. An inverse exists if and only if the determinant is $\ne 0$. Only square matrices have determinants and only square matrices have inverses. The linear system has a unique solution if there is an inverse.

Written:

$det(A)$ or $|A|$.

For a 2 x 2 matrix

$$ \left( \begin{array}{cc}
a & b  \\
c & d \end{array} \right) $$

the determinant is $ad - bc$. For larger matrices,

$$ det(A) = \sum_{j=1}^n (-1)^{i+j} a_{ij} det(A_{ij}) $$

That is, the determinant is the sum or the products of the matrix element and its cofactor, for every element in a row (or column). $i$ is the row, $j$ is the column and $n$ is the number of columns.

### Properties of Determinants

* $$ det(A) = det(A^T) $$

*  If you swap two rows (or columns) of a matrix you multiply the determinant by −1

*  If a matrix has a row (or column) or zeros, then its determinant is 0.

*  If a matrix has two identical rows (or two identical columns) then its determinant is 0.

* If you multiply a row (or column) by a scalar, then you multiply the determinant by that scalar.

*  If you add a multiple of one row (or column) to another row (or column respectively) then the determinant is unchanged.

*  The determinant of a (upper or lower) triangular matrix is the product of the diagonal entries.

* If $A$ and $B$ are square matrices then

$$ det(AB) = det(A)det(B) $$

### Finding the determinant of a matrix

Apply row operations ([Gaussian Elemination](http://localhost:4000/LinearSystems.html#gaussian-elemination)) to get to upper or lower triangular matrix form.

The determinant is the the product of the diagonal entries (of the echelon form) multiplied by −1
for every row swap and α for every row operation of the form Ri := αRi.

Cofactors
----

The *ith*, *jth* cofactor of matrix $A$ is:

$$ -1^{i+j} det(A_{ij}) $$

The $-1^{i+j}$ part is just the sign checkerboard:

$$ \left( \begin{array}{ccc}
+ & - & +  \\
- & + & - \\
+ & - & + \end{array} \right) $$

Classical Adjoint
----

The transpose of the matrix of cofactors. Written:

$$ adj(A) $$

This can be used to find the inverse of a matrix by:

$$ A^{-1} = \frac{1}{det(A)} adj(A) $$

Cramer's Rules
-----

A variable $x_n$ in a system of linear equations with matrix of coefficients $A$ is the ratio of the determinant of the matrix formed by replacing the $n$th column of $A$ with the column of constants, to the determinant of $A$.

Row Space
----

The row space of a $m x n$ matrix is the span of the row vectors $span\{v_1, ..., v_m\}$.

The *basis* of a row space is the rows having a leading entry in a matrix in row-echelon form.

Column Space
----

The column space of a $m x n$ matrix is the span of the column vectors $span\{u_1, ..., u_n\}$.

The *basis* of a column space is found by transposing the matrix, reducing to row echelon form, pick the rows with a leading entry and write them as columns.

or

from row echelon form (of $A$) identify the pivot columns (those with zeros below and to the left) and select the corresponding columns from $A$.

Null Space
-----

The null space of a matrix $A \in M_{mn} (\mathbb{R})$ is the set of vectors that when multiplied by the matrix give the zero matrix:

$$ Ax = 0 $$

Rank
----

The *rank* of a matrix ($rank(A), A \in M_{mn} (\mathbb{R})$) is the dimension of its row space or column space.

The dimension of a matrices row space is always equal to the dimension of its column space.

Rank is equal to the number of pivot columns of a matrix in row echelon form, or the number of dependent variables.

Nullity
-------

The *nullity* of $A$ is the dimension of its *null space*. Equal to the number of free variables in a system of equations.

### Rank-nullity Theorem

For $A \in M_{mn} (\mathbb{R})$,

$$ rank(A) + nullity(A) = n $$

Eigenvalues and Eigenvectors
=======

An **Eigenvalue** $\lambda$ is a scalar such that there is a non zero solution $v$ to the equation:

$$ Av = \lambda v$$

An **Eigenvector** $v$ is a non-zero solution (given $\lambda$) to the equation:

$$ Av = \lambda v$$

The set of all solutions to this equation is called the $\lambda$-eigenspace. I.e. the set of vectors which produce the same value when multiplied by $A$ and $\lambda$ (some Eigenvalue).

E.g.

$$ \left( \begin{array}{cc}
1 & 2 \\
1 & 0 \end{array} \right) \left( \begin{array}{c}
2 \\
1 \end{array} \right) = \left( \begin{array}{c}
4 \\
2 \end{array} \right) = 2 \left( \begin{array}{c}
2 \\
1 \end{array} \right) $$

$2$ is an Eigenvalue for $A$. $\left( \begin{array}{c}
2 \\
1 \end{array} \right)$ is a 2-Eigenvector.

Calculating Eigenvalues and Eigenvectors
---------

$$ Av = \lambda v = (A - \lambdaI)v = 0 $$

(0 is the zero matrix)

$\lambda$ is an Eigenvalue if there is more than one solution, therefore if the determinant is 0. Hence the Eigenvalues of a matrix are the solutions of:

$$ det(A - \lambdaI) = 0 $$

This is called the **characteristic equation**. The roots of the characteristic equation are the Eigenvalues.

Calculating Eigenspaces (sets of Eigenvectors)
------

Once you have an Eigenvalue ($\lambda$) calculate the Eigenvectors for each Eigenvalue.

The λ-eigenspace of a matrix A are the solutions v to the linear system:

$$ (A - \lambdaI)v = 0 $$

Maple
----

Use Maple command to enter as lists:

    Matrix([[1,2,3],[4,5,6]])

or enter columns:

    <<1,4>|<2,5>|<3,6>>

or rows:

    M = <<1|2|3>,<4|5|6>>

Zero based index using square brackets $[row,column]$:

    M[2,3] # 5

Can use ranges:

    M[2, 2 .. 3]

Special matrices:

    ZeroMatrix(n);
    IdentityMatrix(n);

Matrix multiplication:

    3 * M;
    <<1,4>|<2,5>> . <<1,4>|<2,5>>

Augmentation:

    aug:=<a|b>;

Other functions:

    Determinant(M);
    Transpose(M);

TI Nspire
======

Matrix Augmentation:

```
augment(a,b)
```

Add multiples of rows:

```
mRowAdd(factor, matrix, source, target)
```

Swap rows:

```
rowSwap(matrix, source, target)
```

Multiply a row:

```
mrow(5, matrix, target)
```
