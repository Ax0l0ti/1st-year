# Matrix Detriments 
---
*Date :* 09-02-2024
*Module :* #CM12006
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]] 
> [[# ]]
> [[# ]]
> 
--- 
## Overview 

![[RunDownOfUniDetMethod.png]]

where **i = 1** we have the following $det$ **Seen in A level**
$$ \det \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} = a\begin{bmatrix} e & f \\ h & i\\ \end{bmatrix} - b\begin{bmatrix} d & f \\ g & i \\ \end{bmatrix} + c\begin{bmatrix} d & e \\ g & h\\ \end{bmatrix} $$
$$ explained \space signs  = [ (-1)^{(1+1)} = + \space ] ... [ (-1)^{(1+2)} = + \space ] ... [ (-1)^{(1+3)} = - \space ]  $$

where **i = 2** we have the same resultant $det$ but with a different form

$$ \det \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} = d\begin{bmatrix} b & c \\ h & i\\ \end{bmatrix} - e\begin{bmatrix} a & c \\ g & i \\ \end{bmatrix} + f\begin{bmatrix} a & b \\ g & h\\ \end{bmatrix} $$
$$ explained \space signs  = [ (-1)^{(2+1)} = - \space ] ... [ (-1)^{(2+2)} = + \space ] ... [ (-1)^{(2+3)} = - \space ] $$
##### structure
$(m \times n)$ matrix is defined at m rows and n columns.
$$ \begin{bmatrix}
a_{11} & a_{12} & ... & a_{1n} \\
a_{21} & a_{22} & ... & a_{2n} \\
... & ... & ... & ... \\
a_{m1} & a_{m2} & ... & a_{mn} 
\end{bmatrix}  $$

![[StolenDetrimentDefintion.png]]

$\det A = (-1)^{i+1}a_{i1} \det A_{i1} + (-1)^{i+j}a_{ij} \det A_{ij} + ~...~ + (-1)^{i+n}a_{in} \det A_{in}$ is


##### properties of detriment 

let $A^1$ be a matrix obtained from A by swapping positions of 2 different rows. $\det A^1 = - \det A$ 
let $A^1$ be a matrix obtained from A by multiplying a row by number $k$. 
$\det A^1 = - k \det A$ 


--- 

### Det of 2x2 matrix 

the detriment of 2x2 Matrix below is simply $a_{11}a_{22} -a_{12}a_{21} = ad - bc$
$$ A = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}\\
\end{bmatrix} = \begin{bmatrix}
a & b \\
c & d\\
\end{bmatrix}  $$

##### How tf 2x2 works out in Uni terms 
 So the fancy formula is $\det A = (-1)^{i+1}a_{i1} \det A_{i1} + (-1)^{i+j}a_{ij} \det A_{ij} + ~...~ + (-1)^{i+n}a_{in} \det A_{in}$
 But this is basically $\det A = first + other ~ columns + final$

 ---

### Det of 3x3 Matrix


**Inverting a 3x3 matrix**
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

$A^{-1} = {1 \over \det A} C^T$
where $C^T = 
CT.
Each element of the matrix CT is divided by the determinant of A.