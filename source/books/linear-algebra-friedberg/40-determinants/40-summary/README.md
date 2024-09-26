# Summary--Important Facts about Determinants

### Content Notes

**Definitions of Determinant**

1. If $A$ is $1\times 1$, then $\det(A)=A_{11}$, the single entry of $A$.

2. If $A$ is $2\times 2$, then $\det(A)=A_{11}A_{22}-A_{12}A_{21}$.

3. If $A$ is $n\times n$ for $n>2$, then
   $$
   \det(A)=\sum_{j=1}^n(-1)^{i+j}A_{ij}\cdot\det(\tilde{A}_{ij})
   $$
   (if the determinant is evaluated by the entires of row $i$ of $A$) or
   $$
   \det(A)=\sum_{i=1}^n(-1)^{i+j}A_{ij}\cdot\det(\tilde{A}_{ij})
   $$
   (if the determinant is evaluated by the entires of column $j$ of $A$) where $\tilde{A}_{ij}$ is the $(n-1)\times(n-1)$ matrix obtained by deleting row $i$ and column $j$ from $A$.

**Properties of the Determinant**

1. If $B$ is a matrix obtained by interchanging any two rows or interchanging any two columns of an $n\times n$ matrix $A$, then $\det(B)=-\det(A)$.
2. If $B$ is a matrix obtained by multiplying each entry of some row or column of an $n\times n$ matrix $A$ by a scalar $k$, then $\det(B)=k\cdot\det(A)$.
3. If $B$ is a matrix obtained from an $n\times n$ matrix $A$ by adding a multiple of row $i$ to row $j$ or a multiple of column $i$ to column $j$ for $i\ne j$, then $\det(B)=\det(A)$.
4. The determinant of an upper triangular matrix is the product of its diagonal entries. In particular, $\det(I)=1$.
5. If two row (or columns) of a matrix are identical, then the determinant of the matrix is zero.
6. For any $n\times n$ matrices $A$ and $B$, $\det(AB)=\det(A)\cdot\det(B)$.
7. An $n\times n$ matrix $A$ is invertible if and only if $\det(A)\ne0$. Furthermore, if $A$ is invertible, then $\det(A^{-1})=\dfrac{1}{\det(A)}$.
8. For any $n\times n$ matrix $A$, the determinants of $A$ and $A^t$ are equal.
9. If $A$ and $B$ are similar matrices, then $\det(A)=\det(B)$.