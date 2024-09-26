# Systems of Linear Equations--Computational Aspects

### Content Notes

#### Definition

Two systems of linear equations are called **equivalent** if they have the same solution set.

#### Theorem 3.13

Let $Ax=b$ be a system of $m$ linear equations in $n$ unknowns, and let $C$ be an invertible $m\times m$ matrix. Then the system $(CA)x=Cb$ is equivalent to $Ax=b$​.

##### Corollary

Let $Ax=b$ be a system of $m$ linear equations in $n$ unknowns. If $(A'|b')$ is obtained from $(A|b)$ by a finite number of elementary row operations, then the system $A'x=b'$ is equivalent to the original system.

#### Definition

A matrix is said to be in **reduced row echelon form** if the following three conditions are satisfied.

(a) Any row containing a nonzero entry precedes any row in which all the entries are zero (if any).

(b) The first nonzero entry in each row is the only nonzero entry in its column.

(c) The first nonzero entry in each row is $1$ and it occurs in a column to the right of the first nonzero entry in the preceding row.

#### Theorem 3.14

Gaussian elimination transforms any matrix into its reduced row echelon form.

#### Theorem 3.15

Let $Ax=b$ be a system of $r$ nonzero equations in $n$ unknowns. Suppose that $\text{rank}(A)=\text{rank}(A|b)$ and that $(A|b)$ is in reduced row echelon form. Then

(a) $\text{rank}(A)=r$.

(b) If the general solution obtained by the procedure above is of the form
$$
s=s_0+t_1u_1+t_2u_2+\cdots+t_{n-r}u_{n-r}
$$
then $\{u_1,u_2,\dots,u_{n-r}\}$ is a basis for the solution set of the corresponding homogeneous system, and $s_0$ is a solution to the original system.

#### Theorem 3.16

Let $A$ be an $m\times n$ matrix of rank $r$, where $r>0$, and let $B$ be the reduced row echelon form of $A$. Then

(a) The number of nonzero rows in $B$ is $r$.

(b) For each $i=1,2,\dots,r$, there is a column $b_{j_i}$ of $B$ such that $b_{j_i}=e_i$.

(c) The columns of $A$ numbered $j_1,j_2,\dots,j_r$ are linearly independent.

(d) For each $k=1,2,\dots,n$, if column $k$ of $B$ is $d_1e_1+d_2e_2+\cdots+d_re_r$, then column $k$ of $A$ is $d_1a_{j_1}+d_2a_{j_2}+\cdots+d_ra_{j_r}$.

##### Corollary

The reduced row echelon form of a matrix is unique.

### Selected Exercises

#### 15

If $B$ and $B'$ are both reduced row echelon form of $A$, consider column $k$ of $B$ and column $k$ of $B'$, use Theorem 3.16(a) we know there exists scalars $d_i$ and $d_i'$ such that
$$
B_k=d_1e_1+\cdots+d_re_r,\quad B_k'=d_1'e_1+\cdots+d_r'e_r
$$
thus
$$
A_k=d_1a_{j_1}+d_2a_{j_2}+\cdots+d_ra_{j_r}=d_1'a_{j_1}+d_2'a_{j_2}+\cdots+d_r'a_{j_r}
$$
use Theorem 3.16(c), we have $d_i=d_i',1\le i\le r$, this means $B_k=B_k'$, this is true for any $k$, thus $B=B'$.

### Summary

本节利用初等行变将线性方程组系统变为同样解集合但是更容易解出来的新方程组。