# Gaussian elimination
---
*Date :* 10/03/24
*Module :* #CM12006 
*Teacher*:  
*Resources :*

---
##### Contents: 
> [[# ]]  [[#ChatGPT notes]]
> [[# ]]

--- 
##### ChatGPT notes 
**Prompt : Teach me about Gaussian elimination** 

**Response :**
Gaussian elimination is a method used to solve systems of linear equations by transforming the augmented matrix representing the system into row-echelon form (or reduced row-echelon form). This process involves a sequence of elementary row operations, including row swaps, row scaling, and row additions.

Let's illustrate Gaussian elimination with an example. Consider the following system of linear equations:

Given the system of linear equations: $$ \begin{cases} 2x + 3y - z = 4 \\ 3x + 2y + z = 5 \\ x - y + 2z = 1 \end{cases} $$ We represent this system as an augmented matrix: $$ \left[ \begin{array}{ccc|c} 2 & 3 & -1 & 4 \\ 3 & 2 & 1 & 5 \\ 1 & -1 & 2 & 1 \end{array} \right] $$ Now, let's proceed with Gaussian elimination: Make the elements $( a_{N1} )$ equal to zero where $N \gt 1$.  $R_2 = R_2 - \frac{3}{2}R_1$  and $R_3 = R_3 - \frac{1}{2}R_1$
 This operation results in: $$\left[ \begin{array}{ccc|c} 2 & 3 & -1 & 4 \\ 0 & -\frac{5}{2} & \frac{5}{2} & -1 \\ 0 & -\frac{5}{2} & \frac{5}{2} & -1 \end{array} \right] $$ 3. **Step 3**: Now, we'll eliminate the $( a_{N2} )$ element where $N \gt 2$. To do this, we'll subtract the second row from the third row. $$ R_3 = R_3 - R_2 $$ This operation results in: $$ \left[ \begin{array}{ccc|c} 2 & 3 & -1 & 4 \\ 0 & -\frac{5}{2} & \frac{5}{2} & -1 \\ 0 & 0 & 0 & 0 \end{array} \right] $$ Now, our matrix is in **row-echelon form**. We can proceed to back-substitution to find the values of $( x ), ( y )$, and $( z )$. 
 
 1. From the last equation, we see that $(0x + 0y + 0z = 0)$, which tells us nothing new. 
 2. From the second equation, we have $(-\frac{5}{2}y + \frac{5}{2}z = -1)$, which simplifies to $(y - z = \frac{2}{5})$. 
 3. From the first equation, we have $(2x + 3y - z = 4)$. Substituting $(y - z = \frac{2}{5})$, we can solve for $(x)$. 
 
 By solving these equations, we find the values of $(x), (y)$, and $(z)$, which represent the solution to the original system of equations. $$\begin{align*} x &= \frac{7}{5} - t \\ y &= \frac{2}{5} + t \\ z &= t \end{align*}$$
 These values represent the solution to the system of equations in terms of the parameter $(t)$. **Vector space**

$\begin{bmatrix} x \\ y \\ z \end{bmatrix} = \begin{bmatrix} 7/5 \\ 2/5 \\ 0 \end{bmatrix} + t\begin{bmatrix} -1 \\ 1 \\ 1 \end{bmatrix}$


