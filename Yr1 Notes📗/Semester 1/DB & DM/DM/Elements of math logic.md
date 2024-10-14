# Elements of math logic
---
> [!info]+ File Details
> Includes information about this (genus:: Note). Contains details on when this was created, what module the note belongs to.
> > *Date :*  03-10-2023 
> > *Module :* (ModCode :: CM12004DM)
> > *Teacher*:  [Nicolai Vorobjov](https://moodle.bath.ac.uk/user/profile.php?id=2806)
> > *Resources :

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Logical Connectives]]
> [[#Boolean Formulae]]
> [[#Tautoligies]]
> [[#Boolean Laws]]
> [[#Direct and inverse theorems]]
> [[#Disjunctive normal form DNF of a Boolean formula]]
> [[#Conjuctive normal form of a Boolean formula]]
--- 

Proposition can have values of true(t) or false(f) but not at the same time. 

### Logical Connectives
1. **Conjuction** (logical AND). It is denoted by the symbol $(\wedge)$. Conjection is only true if both propositions (X & Y) are true.
$$ 
\begin{array}{ccc}
x&y&x\wedge y\\ 
t& t& t \\  
f& f& f \\
t& f& f \\
f& t& f \\
\end{array} 
$$
2. **Disjunction** (logical OR). It is denoted by $\vee$. It is only false when both propositions are false. 
$$ \begin{array}{ccc} x&y&x\vee y\\ t& t& t \\  t& f& t \\f& t& t \\ f& f& f\\ \end{array} $$

3. **Implication** (logical if-then). It is denoted by $\rightarrow$ .  X is called the assumption and y is called the consequence. It is read as "if x then y". 
$$ \begin{array}{ccc} x&y&x\rightarrow y\\ t& t& t \\ t& f& f \\ f& t& t \\ f& f& t \\ \end{array} $$

4. Negation (logical NOT). It is denoted by $\neg$ . 
$$\begin{array}{rcl} x & \neg x \\ t & f \\ f & t \\ \end{array}$$
--- 
### Boolean Formulae
**Definition:** 
Let symbols X<sub>1</sub>,X<sub>2</sub> . . . , X<sub>n</sub> be variables. Boolean formula is a string of symbols from the set {X1, . . . , Xn, ∧, ∨, →, ¬,(,)} such that
	1. Any variable X<sub>i</sub> , (1 ≤ i ≤ n) is a Boolean formula. 
	2. If F and G are two Boolean formulae, then expressions (F ∧ G), (F ∨ G), (F → G) and ¬F are Boolean formulae.

e.g (X → ¬Y ) ∨ (¬Z ∧ Y ) is a boolean formulae but (X →)) is not. This is because the consequence is missing and parentheseis are unbalanced. 

---
### Tautoligies
**Definition:**
A Boolean formula F with variables X<sub>1</sub>, X<sub>2</sub> . . . , Xn is called identically true or tautology if for any assignment of true/false values to variables the value of F is t. Similar to identically false formula. 
e.g. 
	- X ∨ ¬X -- Tautology
	- ¬¬X → X -- Tautology
	- ((¬X → Y ) ∧ (¬X → ¬Y )) → X

We can write (F → G) ∧ (G → F) as F ≡ G where F and G are some Boolean formulae. 

^ and V is a commutative operation. So we can say that F^G ≡ G^F ||| F V G ≡ G V F. 
^ and V are also associative operations. So we can write BFs as ((X ∧ Y ) ∧ Z) ≡ (X ∧ (Y ∧ Z))


---
### Boolean Laws
**==Distributive laws ==**
	**Conjection over disjunction.** For variables X, Y , Z the Boolean formula below is identically true.  $$ (X ∧ (Y ∨ Z)) ≡ ((X ∧ Y ) ∨ (X ∧ Z)) $$
	**Disjunction over conjunction.** For variables X, Y , Z the Boolean formula the formula below is identically true. $$ (X ∨ (Y ∧ Z)) ≡ ((X ∨ Y ) ∧ (X ∨ Z))$$


##### ==De Morgan's Laws==
$$ ¬(X ∧ Y ) ≡ (¬X ∨ ¬Y ) $$ $$ ¬(X ∨ Y ) ≡ (¬X ∧ ¬Y ) $$
For the variable X, Y the above boolean formulaes are identically true. 


##### Some other laws of logic
1. The law below shows how $\rightarrow$ can be replaced with $\cup$ to make solving equation easier. $$ (X → Y ) ≡ (¬X ∨ Y ) $$
Both statements above are false thus equivalent. We know this by assigning true/false values to X and Y accordingly. If X then Y  is only true if both values are true. 

2. ¬¬X ≡ X . Double negation leads to the origianal variable. 

Every Boolean formula is equivalent to a formula having only one of the following pairs of connectives:  ¬, ∧ or  ¬, ∨ or ¬, →.


---
### Direct and inverse theorems
Many mathematical theorems can be described as implications $X → Y$. Call this implication direct theorem. Then the proposition $Y → X$ is known as inverse theorem. Even if the direct theorem is true, the inverse may or may not be true. 
For example: 
	If a number is divisible by 6$(X)$ then it is divisible by 3 $(Y)$, $X\rightarrow Y$. This statement is true. 
	However if we say $Y\rightarrow X$ (inverse statement) the statement becomes false. Number divisible by 3 isn't always divisible by 6. 


The proposition $¬X → ¬Y$ is called opposite theorem. The proposition $¬Y → ¬X$ is, therefore, opposite to inverse theorem. Observe, that an opposite to inverse theorem is true if and only if the direct theorem is true, because of the tautology $X \rightarrow Y \equiv \neg Y \rightarrow \neg X$.
For example: 
	$\neg X \rightarrow \neg Y$ (Opposite Statement) . If anumber is not divisible by 6 then it is not divisble by 3. 
	$\neg Y \rightarrow \neg X$ Opposite to inverse. If a number is not divisible by 3 then it is not divisible by 6. 

---
### Disjunctive normal form (DNF) of a Boolean formula

Let $X_1$, $X_2$ , . . . , $X_n$ be variables. $Y_i$ is called a literal if $Y_i$ is either $X_i$ or $\neg X_i$ for any $i$. 
A conjunctive term is a conjunction of the kind $Y_{i1} ∧ Y_{i2} ∧ · · · ∧ Y_{im}$, where $i_j$ is one of the numbers 1, 2, . . . , n for 1 ≤ j ≤ m, and each $Y_{ij}$ is a literal. 

**Definition:** A Boolean formula F is in disjunctive normal form (DNF) if F is of the form $F_1 ∨ F_2 ∨ · · · ∨ F_k$, where $F_i$ is a conjunctive term for any i.
> So in simple words its disjunction (OR) of Conjuctive (AND) terms. 

---
### Conjuctive normal form of a Boolean formula

Disjunctive clause (or just clauses) is simply disjunction of literals. e.g $Y_i \cup Y_i2 \cup (Y_i)_n$  

**Definition:** A Boolean formula F is in conjuctive normal form(CNF) if F is of the form $F_1 \wedge F_2 \wedge ... \wedge F_K$ where $F_i$ is a disjunction term for any $i$.  
> So in simple words its conjuction (AND) of disjunctive (OR) terms. 


> We use literals to maek conjunctive clauses and conjuctive clauses to make disjunctive normal form. 

---