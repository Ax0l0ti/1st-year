# Proof
---
*Date :*  23-10-2022 
*Module :* #CM10311 
*Teacher*:  
*Resources :*

---
##### Contents: 
> [[#Proof by induction]]
> [[# ]]
> [[# ]]
> 
--- 

### Proof by induction
###### Example 1
The use of induction method is illustrated below by proving the formula for the sum of geometric progression. 
$$ 1 + q + q^2 + ...+q^n = \frac{q^{n+1}-1}{q -1} $$
for all integer $q \neq 1$ and $n \ge 0$. As for this example we will conduct induction on $n$. 

**Base**: For $n=0$ the formula above is true since both sides are equal to 1. 
**Inductive hypothesis**: Assume that the formula above is true. 
**Inductive step**: We need to prove that:
$$ 1 + q + q^2 + ...+q^{n+1} = \frac{q^{n+2}-1}{q -1}  $$
By inductive hypothesis, the sum of first $n + 1$ terms in the left-hand side of the second formula equals to $1 + q + q^2 + ...+q^n = \frac{q^{n+1}-1}{q -1}$ . 
Therefore, the left-hand side of the second formula can be re-written as 
$$\frac{q^{n+1}-1}{q -1} + q^{n+1}$$ which is equal to right-hand side of the second formula. This completes the proof of the first formula.
###### Example 2
Squares grow faster than linear functions. Prove the inequality $n+2 \le n^2$ for all integer numbers $n \ge 2$. 
**Base**: For n=2 the inequality is obviously true. 
**Inductive hypothesis**: Assume that $n+2 \le n^2$ for some $n \ge 2$. 
**Inductive Step**: We prove that $(n+1)+2 \le (n+1)^2$. The right side is equivalent to $n^2 - (n+2) +2n \ge 0$. By the inductive hypothesis, $n^2 - (n+2) \ge 0$ but obiviously $2n>0$ so the required inequality is true. 