# (Partial) Orders
---
*Date :*  14-11-2023 
*Module :* #CM12004DM 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#Arithmetic of real numbers]]
> [[#Reflexive, symmetric & Transitive]]
> [[#Partial order and total order]]
> [[#Maximal and minimal elements]]
> 
--- 

### Arithmetic of real numbers
**Definition**: Let $x,y \in R$. $x+y$ and $xy$ are defined as follows. 
- Choose a Cauchy sequence, $\{a_n\}\in x$ and $\{b_n\} \in y$ 
- Then $x+y$ is the real number containing the sequence $\{a_n\}+\{b_n\}$. 
- Similarly, $xy$ is the real number containing the sequence $\{a_n\}\cdot\{b_n\}$


### Reflexive, symmetric & Transitive

#### Reflexive $aRa$  
- **Definition:** A relation $R$ on a set $A$ is said to be reflexive if, for ==**every**== element $x$ in $A$, the ordered pair $((a,a))$ belongs to $R$.
- **Explanation:** In simpler terms, a relation is reflexive if every element in the set is related to itself. This means that for any element $x$ in the set $A$, the statement $aRa$ holds true.
Opposite - TODO Irreflexive 
#### Symmetric $aRb \implies bRa$
-  **Definition:** A relation $R$ on a set $A$ is said to be symmetric if, for every ==**pair**== of elements $a$ and $b$ in $A$, if $(a,b)$ belongs to $R$, then $(b,a)$ also belongs to $R$.
- **Explanation:** In simpler terms, a relation is symmetric if whenever $a$ is related to $b$, then $b$ is also related to $a$. This implies that if $aRb$ holds, then $bRa$ must also hold.
Opposite - Asymmetric
#### Transitive $aRb \vee bRc \implies bRa$
- **Definition:** A relation $R$ on a set $A$ is said to be transitive if, for every ==**triple**== of elements $a$, $b$ and $c$ in $A$ , if $(a,b)$ belongs to $R$ and $(b,c)$ belongs to $R$, then $(a,c)$ also belongs to $R$.
- **Explanation:** In simpler terms, a relation is transitive if whenever $a$ is related to $b$, and $b$ is related to $c$, then $a$ is also related to $c$. This implies that if $aRb$ and $bRc$ hold, then $aRc$ must also hold.
Opposite - TODO

### Partial order and Strict Partial order

>**Definition**: A relation R on set $A$ is called partial order on $A$, if $R$ is:
>	- Reflexive
>	- Antisymmetric
>	- Transitive

Examples:
	1) Relation $≤$ on $Z$ is a partial order. 
	2) Relation $≥$ on $Z$ is a partial order. 
	3) Relation $=$ on $Z$ is a partial order.
	4) Relation $<$ on $Z$ is not a partial order (antisymmetric and transitive, but not reflexive)  
	5) Relation $⊂$ on the set $A$ of all subsets of a universe $U$ is a partial order on $A$. 
	6) Let A = {∅, {a}, {b}, {a, b}, {a, c}, {b, c}}. The relation ⊂ is a partial order on A.

**Definition**: Let $A$ be a set. A relation R on $A$ is called **antisymmetric** if conditions $(x,y) \in R$ **and** $(y,x) \in R$ imply $x=y$, for all $x,y \in A$. 
Examples: 
	1) Relation $≤$ on $Z$ is antisymmetric. 
	2) Relation $<$ on $Z$ is also antisymmetric (because the proposition $(x < y) ∧ (y < x)$ is false for all pairs $x, y ∈ Z$, hence the implication $((x < y) ∧ (y < x)) → (x = y) is \ true)$

> **Definition**: A partial order $R$ on $A$ is called total order if for any $x,y \in A$ either $(x,y) \in R$ or $(y,x) \in R$ is true. 

Examples:
	1) Relation $≤$ on $Z$ is a total order. 
	2) Let $A = \{∅, \{a\}, \{a, b\}, \{a, b, c\}, \{a, b, c, d\}\}$. The the relation $⊂$ is a total order on $A$.

### Quick table of Strict vs Partial Order 

| Partial Order | Strict P.O  |
| ------------- | ----------- |
|   Reflexive   | Irreflexive |
|   Symmetric   | Asymmetric  |
|   Transitive  | Transitive  |
### Maximal and minimal elements

>**Definition**: Let $R$ be a partial order on $A$. Element $x \in A$ is called maximal if $\forall y \in A ((x,y)\in R \to x = y)$ 

> **Definition**: Element $x\in A$ is called minimal if $\forall y \in A ((y,x) \in R \to x = y)$ 

Example:
	$A  = \{1,2,3\}$ check $R$: $\ge$ *(checking maximal)*
	We claim that $3$ is the maximal element. 
	Now we check the formula in the maximal definition with each $y$. 
	$(3 \le 1) \to (3=1)$
	$(3 \le 2) \to (3 = 1)$
	$(3 \le 3) \to (3 = 3)$
	All of the statements above are **True** because of implication and boolean concepts. 

### Strict Partial Order
>**Definition**: $R$ is called strict partial order if:
>	- $R$ is asymmetric
>	- $R$ is transitive

Example: $(< on \ Z)$ is asymmetric

**Definition**: Let $R$ be a partial order on set $A$. $A$ is called **asymmetric** if either $(x,y) \notin R$ or $(y,x) \notin R$ for all pairs $x,y \in A$. 
*Definition meaning it is not True that $(x,y) \in R$ and $(y,x) \in R$*

**Theorem**: Let $A$ be a set. 
1. If $\le$ be partial order on $A$ then a relation $<$ on A is defined by: $x<y \ if \ (x \le y) \wedge (x \ne y)$ is a strict partial order on A. 
2. If $<$ is strict partial order on A, then the relation $\le$ on $A$ is defined by $(x \le y) \ if \ (x < y) \vee (x = y)$ is partial order on $A$. 

**Proof**: 
We need to prove that $<$ is asymmetric and transitive
**Asymmetric**: Suppose that, $(x < y) ∧ (y < x)$ is true for some $x, y ∈ A$. Then, by the definition of $<, (x ≤ y) ∧ (y ≤ x)$. Since the relation $≤$ is antisymmetric, it follows that $x = y$, which contradicts to x $<$ y in view of the definition of $<$. 
**Transitive**: $(x < y) \wedge (y < z)$ need to prove: $x < z$
By definition of $<: (x \le y) \wedge (y \le Z)$. By transitivity of $\le$ we have $x \le z$. Suppose $x \le z$, then $(z \le y) \wedge (y \le z )$, by asymmetry, $y = z$. 



### Divisiblity of integers
Let $Z$ denote the set of all integers. 

**Definition**: Two non-zero integers $a,b \in Z$ are called relatively prime if their greatest common divisor(GCD) $(a,b) = 1$. 
Example: 5,6 are relitively prime numbers
	Divisiors of 5 are {1,5}
	Divisors of 6 are {1,2,3}
	Hence their GCD is 1
Theorem: $a,b \in Z$ are relitively prime if and only if there exists $u,v \in Z$ such that $au + bv = 1$. 

**Definition**: For $a, b, m ∈ Z, m > 0$, we say that $a$ is congruent to $b$ modulo $m$ and write $a ≡ b$ mod m, if $a − b$ is divisible by $m$. Equivalently, $a ≡ b$ mod m if $a$ is divisible by $m$ with the same remainder as is b divisible by $m$. 