# Eigen vectors & Eigen values
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :* 21/03/24
> > *Module :* (ModCode :: CM12006) 
> > *Teacher*: 
> > *Resources :* drive

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#WTF is an eigenvector]]
> [[#Finding Diagonal Form]]
> [[#Eigenvalues from Diag Form ]]

--- 
## WTF is an eigenvector 

1. An **eigenvector** of a **matrix $A$** is a non-zero column vector x which satisfies the equation **$Ax = \lambda x$**, where $\lambda$ is a scalar.
The value of the scalar 2 is the **eigenvalue** of the matrix corresponding to the **eigenvector $x$.**
2. If x is an eigenvector of a matrix $M$ representing a linear transformation, then the straight line that passes through the origin in the direction of $x$ is an **==invariant line==** under that transformation.
3. The equation **det(A - I) = 0** is called the characteristic equation of $A$. The solutions to the characteristic equation are the eigenvalues of $A$.
4. If $a= \begin{bmatrix} a \\ b \end{bmatrix}$ is an eigenvector of a matrix $A$, then the unit vector  $â= \begin{bmatrix} \frac{a}{|a|} \\ \frac{b}{|b|} \end{bmatrix}$ is a ==**normalised eigenvector**== of $A$.
5. A diagonal matrix is a square matrix in which all of the elements which are not on the diagonal from the top left to the bottom right of the matrix are zero. The diagonal from the top left to the bottom right of the matrix is called the **leading diagonal**.

$$ \text{The general 2 x 2 diagonal matrix is} \begin{bmatrix} a & 0 \\ 0 & b \end{bmatrix}$$
## Finding Diagonal Form
6. To reduce a given matrix $A$ to diagonal form, use the following procedure:
	• Find the eigenvalues and eigenvectors of $A$.
	• Form a matrix $P$ which consists of the eigenvectors of $A$.
	• Find $P^{-1}$
	• A diagonal matrix D is given by $P^{-1}AP$.

## Eigenvalues from Diag Form
7.  When you reduce a matrix $A$ to a diagonal matrix $D$, the elements on the diagonal are the eigenvalues of $A.$

---