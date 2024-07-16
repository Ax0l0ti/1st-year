# Congruences
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :*  25-11-2023 
> > *Module :* #CM12004DM
> > *Teacher*: 
> > *Resources :* [Congruence Modulo m (Theory) - YouTube](https://www.youtube.com/watch?v=-SpWfD4WsmM&ab_channel=NesoAcademy), [Solving congruences, Simple examples - YouTube](https://www.youtube.com/watch?v=KwxslifHITg&ab_channel=blackpenredpen), [Congruences Complex example - YouTube](https://www.youtube.com/watch?v=LInNgWMtFEs&ab_channel=blackpenredpen)

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Divisiblity of Integers]]
> [[#Division operation in $ frac{Z}{mZ}$]] 
> [[# ]]
--- 

#### Divisibility of Integers

**Definition**: For $a, b, m ∈ Z, m > 0$, we say that $a$ is congruent to $b$ modulo$m$ and write $a ≡ b$ mod m, if $a − b$ is divisible by $m$. Equivalently, $a ≡ b$ mod $m$ if $a$ is divisible by $m$ with the same remainder as is $b$ divisible by $m$.

**Proposition 1**: Let for $a, m ∈ Z, m > 0$, an integer $r$ be the remainder of the division of $a$ by $m$. Then $a ≡ r$ mod $m$.

**Proposition 2**: Fix $m\in Z$. The relation "congruent module $m$" is an equivalence relation. That is:
	- $a \equiv a$ mod m;
	- if $a\equiv b$ mod m, then $b \equiv a$ mod m;
	- if $a \equiv b$ mod $m$ and $b \equiv c$ mod $m$ , then $a \equiv c$ mod $m$. 

###### More properties of congruences
**Proposition 3**: If $a ≡ b$ mod $m$ and $c ≡ d$ mod $m$, then $a + c ≡ b + d$ mod $m$ and $ac \equiv bd$ mod $m$. 

###### Division operation in $\frac{Z}{mZ}$ 
In this unit we introduced various number systems: Z (integers), Q (rationals), R (reals), and, finally, $Z/mZ$ (integers modulo m).

In each of these sets we have inverse element with respect to addition (additional inverse)
$x+y = 0$ (identity element with respect to $+$). We denote $y$ by $-x$. 

$y$ is multiplicative inverse of $x$ if $x \cdot y = 1$ in $Z$. Multiplicative inverse element $y$ is denoted by $x^{-1}$. 

**Proposition 5**: An element $x ∈ Z/mZ$ has multiplicative inverse if and only if integers in residue class of $x$ are relatively prime with $m$.

Proof: Let $x$ have $x^{-1}$ i.e, there are $a \in x$ and $b \in Z$ such that $a \cdot b \equiv 1$ mod $m$. 
Let $GCD (a,m) \equiv d$. 
$m | (ab - 1)$. Implies $d | (ab-1)$, but $d | a$ heres $d|a$, then $d | 1$. We conclude that $d=1$. 

Conversly, if $GCD(a,m) = 1$ where $(a\in x)$, then there are $u,v \in Z$ such that $ua + vm = 1$.
As $x^{-1}$ take $[u]$, $ua \equiv 1$ mod $m$ 

E.X:
	m = 5 - prime
	Each element $x \in \frac{Z}{5Z}$ has a multiplicative inverse
	$[3]^{-1} = ?$ 
	$GCD(5,3) = 1$, take $u = 2, v = -1$  then $3u + 5v = 1$ 
	$[3]^{-1} = [2]$ ; $3 \cdot 2 = 6 \equiv 1 \ mod \ 5$. 

If $m$ is prime number, then any $\ne 0$ element in $\frac{Z}{mZ}$ then $\frac{x}{y}$ is defined $=x \cdot y^{-1}$.

---