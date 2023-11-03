# Quantifiers
---
*Date :*  23-10-2022 
*Module :* #CM10311 
*Teacher*:  
*Resources :*

---
##### Contents: 
> [[#Universal quantifier]]
> [[#Existential quantifier]]
> [[#∀ and ∃ in the same formula]]
> [[#Negation of quantifiers]] 
--- 

### Universal quantifier

For all numbers x in $A = \{-1, 0, 1 \}$ the inequality $x+1>x$ is true. 
We can rewrite the proposition using just conjunctions: (−1 + 1 > −1) ∧ (0 + 1 > 0) ∧ (1 + 1 > 1).

The first statement can also be expressed in the form $∀x ∈ \{−1, 0, 1\}(x + 1 > x)$
The symbol $\forall$ is read as forall. $\forall$ is called universal quantifier. 

The expression with the universal quantifier is important as it allows us to express large/infinite sets. For example let $Z$ be a set containing all integer numbers. This can be written as $∀x ∈ Z(x + 1 > x)$ 

Expressions such as $x+1 > x$ are called predicate. Predicate  is a "variable" proposition whose truth value changes based on what the variable is. $x$ can take any values; we assigned integers before but can be anything. 

Predicate: Person $X$ is intelligent. This statement is not a proposition because the truth value changes based on who $X$ is. We can turn this predicate statement into a proposition by expressing it as follows: 
	$\forall X \in (\text{Bath Students})\text{(Person X is intelligent)}$
	Here the "Bath Students" is the variable. Hence it can be considered a proposition.

### Existential quantifier
Consider the proposition where $x$ is from the set $A = \{-1,0,1\}$ such that $x\le0$. We can rewrite the proposition using disjunctions $(−1 ≤ 0) ∨ (0 ≤ 0) ∨ (1 ≤ 0)$ 

As with the universal quantifier a larger/infinte set of $A$ would lead to larger disjunction which is difficult to write. Instead we write it in the following form: $\exists x \in A(x \le 0)$. 
∃ is the existential quantifier. As with the universal quantifier, adding $∃x$ to a predicate depending on a variable $x$ turns this predicate into a proposition.
e.g. $∃x ∈ \text{(set of all Bath students) (person x is intelligent)}$ is a proposition. 


### ∀ and ∃ in the same formula

$\forall x \in A, P(x) \rightarrow$ For all x from the set A 
$\exists y \in B, Q(x) \rightarrow$ There exists y in set B 

Given the proposition, $\forall x \in\{-1,0,1\} \exists y \in \{-1,0,1\}(x+y=0)$ the $\exists y \in \{4,0,1\}(x+y=0)$  can be described as "there exists y in this set such that (x+y) = 0"

### Negation of quantifiers
Negation of quantifiers are generalizations of De Morgan’s laws. For example,
$$\begin{array}{}
\neg(\forall x \in \{−1, 0, 1\} (x + 1 > x)) \\
¬((−1 + 1 > −1) ∧ (0 + 1 > 0) ∧ (1 + 1 > 1)) \\
(−1 + 1 ≤ −1) ∨ (0 + 1 ≤ 0) ∨ (1 + 1 ≤ 1)
\end{array}
$$
So from negation we get the proposition which can be defined by ==$∃x ∈ {−1, 0, 1}(x + 1 ≤ x)$==. 
We switched the quantifiers and the > sign when we negated the proposition. 

So in general the rule can be defined as:
- Let M be a set and P(x) be a predicate
	- $(\neg \forall x \in M, P(x)) \equiv (∃x \in M (\neg P(x)))$
	- $(\neg ∃x \in M, P(x)) \equiv (\forall x \in M (\in P(x)))$
Example: 
	$$\begin{array}{}
	\neg(\forall \in M \exists y \in N, P(x,y)) \\
	\exists x \in M \neg(\exists y \in N, P(x,y))\\
	\exists x \in M \forall y \in N \neg P(x,y)
	\end{array} $$
