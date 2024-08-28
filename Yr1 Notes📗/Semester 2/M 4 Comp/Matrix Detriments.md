# Matrix Detriments
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :* 09-02-2024
> > *Module :* #CM12006
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Relation to A-Level]] 
> [[#Det of 2x2 matrix]]
--- 
## Relation to A-Level 

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
\end{bmatrix} $$

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