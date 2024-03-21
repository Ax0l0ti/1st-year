# Inverting Matrices
---
*Date :* 10-01-24
*Module :* #CM12006 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]]  [[#Inverting a 2x2 matrix]]
> [[#Inverting a 3x3 matrix]]

--- 
## Inverting a 2x2 matrix

$$ A = \begin{bmatrix} 
a & b \\ 
c & d \end{bmatrix} \text{ and the inverse of A is }A^{-1} = \begin{bmatrix} 
d & -b \\ 
-c & a \end{bmatrix}  $$
 ---
## Inverting a 3x3 matrix
Finding the inverse of a $3 \times 3$ matrix is more complicated. You need to know the following definition.
- The transpose of a matrix is found by interchanging the rows and the columns.
The transpose of the matrix $M$ is written as $M^T$.
- Finding the inverse of a $3 \times 3$ matrix $A$ usually consists of the following 5 steps.
1. Find the determinant of $A$, $\det A$.
2. Form the matrix of the minors of $A$. In this chapter, the symbol $M$ is used for the matrix of the minors unless this causes confusion with another matrix in the question.
In forming the matrix of minors, $M$ , each of the nine elements of the matrix $A$ is replaced by its minor.
3. From the matrix of minors, form the matrix of cofactors by changing the signs of some elements of the matrix of minors according to the rule of alternating signs illustrated by the pattern
$$\begin{bmatrix} 
+ & - & + \\ 
- & + & - \\ 
+ & - & + \end{bmatrix}$$
Notation $A$ cofactor is a minor with its
appropriate sign.
The symbol $C$ is used for the matrix of the cofactors unless this causes confusion with another matrix in the question.
4. Write down the transpose, $C^T$, of the matrix of cofactors.
5. The inverse of the matrix $A$ is given by the formula

$A^{-1} = {{1}\over{\det A}}C^T \\ \space where \space C^T =$ Cofactor Matrix applied to transposed Matrix of Minors   $\begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix} \text{ is the Cofactor Matrix formed from -1 powers around row 1 }$
