# Cramer's Rule
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :* 25-02-2024
> > *Module :* #CM12006 
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[# ]]  [[#Summary]]
> [[# ]]

---
### Summary

Given the equation in form $Ax = b$ written as $\begin{bmatrix} a_1 & b_1 & c_1 \\ a_2 & b_2 & c_2 \\ a_3 & b_3 & c_3 \end{bmatrix} \begin{bmatrix}x \\ y \\ z \end{bmatrix} = \begin{bmatrix} d_1 \\ d_2 \\ d_3 \end{bmatrix}$

Cramer's rule states that solutions $[ X, Y, Z ] = [ {{D_x}\over{D}} , {{D_y}\over{D}}, {{D_z}\over{D}} ]$ where $D_x$ , $D_y$ and $D_z$  are calculated by replacing their correspondent columns with 

| Value | Calculation |  | Variable | Equation |
| ---- | ---- | ---- | ---- | ---- |
| **$D$** | $\det \begin{bmatrix} a_1 & b_1 & c_1 \\ a_2 & b_2 & c_2 \\ a_3 & b_3 & c_3 \end{bmatrix}$ |  |  |  |
| **$D_x$** | $\det \begin{bmatrix} d_1 & b_1 & c_1 \\ d_2 & b_2 & c_2 \\ d_3 & b_3 & c_3 \end{bmatrix}$ |  | $x$ | ${{D_x}\over{D}}$ |
| **$D_y$** | $\det \begin{bmatrix} a_1 & d_1 & c_1 \\ a_2 & d_2 & c_2 \\ a_3 & d_3 & c_3 \end{bmatrix}$ |  | $y$ | ${D_y}\over{D}$ |
| **$D_z$** | $\det \begin{bmatrix} a_1 & b_1 & d_1 \\ a_2 & b_2 & d_2 \\ a_3 & b_3 & d_3 \end{bmatrix}$ |  | $z$ | ${D_z}\over{D}$ |


[Cramer's rule - Wikipedia](https://en.wikipedia.org/wiki/Cramer%27s_rule)

---