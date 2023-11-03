# Elements of set theory
---
*Date :*  10-10-2022 
*Module :* #CM10311 
*Teacher*:  [Nicolai Vorobjov](https://moodle.bath.ac.uk/user/profile.php?id=2806)
*Resources :*

---
##### Contents: 
> [[#Sets ]]
> [[Quantifiers#Universal quantifier |Universal quantifier]]
> [[Quantifiers#Existential quantifier |Existential quantifier]]
> [[Quantifiers#∀ and ∃ in the same formula |∀ and ∃ in the same formula ]]
> [[Quantifiers#Negation of quantifiers |Negation of quantifiers]]
> [[#Subsets, Equal sets]]
> [[#Union and intersection of sets]]
> [[#Difference of Sets]]
> [[#Cartesian product of sets]]
> [[#Sets of Sets]]
> [[#Power Set]]
--- 
### Sets
Set is a collection, family, class or totality. Each set conists of elements. e.g a set of integer numbers. 
If the set is small we write all elements inside braces. e.g. $S = \{a, b, c\}$. 
In contrast, if a set S is large/infinite we describe this set by the property which is satisfied exactly by elements of S. e.g. $Z = x | \text{x in an integer number}$ 

To express the fact that an element a belongs to a set S, we write a ∈ S. If an element z is not in S, we write $z\notin s$.

Empty set, containing no elements, is denoted by ∅. So, ∅ = { }.

### Subsets, Equal sets
![350](https://www.onlinemathlearning.com/image-files/set-operations-venn-diagrams.png)

Definitions: 
	- Set A is a ==**subset**== of B (A $\subset$ B) if every element in A is also an element in B. $\forall x \in A (x \in B))$  
	- Sets A and B are ==**equal**== if $(A \subset B) \wedge (B \subset A)$ 

For a particular application in set theory, it is convinient to consider all sets as subsets of one large set universe (U). If $A \subset U$ and $B\subset U$, then $A \subset B$ if and only if $\forall x \in U ((x \in A) \rightarrow (x \in B))$. 

### Union and intersection of sets

Definition: For two sets A and B, the set $A ∪ B = \{x|(x ∈ A)∨(x ∈ B)\}$ is called their **==union==**. 
For example:
	- $E \subset Z \rightarrow$ set of even numbers
	- $O \subset Z \rightarrow$ set of odd numbers
	- $\therefore E \cup O = Z$ 
- Example 2
	- Number $P \in Z$ such that $P > 1$ is called prime if it's only positive divisors are 1 and P. 
	- Let P be teh set of all primes. 
	- Then, $O \cup P = O \cup \{2\}$ 

Definition: For two sets A and B, the set $A ∩ B = \{x|(x ∈ A)∧(x ∈ B)\}$ is called their **==intersection==**.
For example:
	- $E \cap O = \emptyset$ (where E is even numbers and O is odd numbers)
	- $E \cap Z = E$ 
For union and instersection all of the boolean laws apply. We just read them differently and use different symbols but the main operation is the same. All these laws apply: 
	- Commutative laws
	- Associative laws
	- Distributive laws
For more see [[Elements of math logic#Boolean Laws]]

### Difference of Sets
Definition: For two sets A and B, the set $A \setminus B = \{x | (x \in A) \wedge (x \notin B)\}$ is called difference of A and B is called difference of A and B. 
If sets A,B,C etc... are subset of the universe U. Then $U \setminus A$ is called the complement of A and denoted by $A'$. 

###### Proof of De Morgan laws.  
$$\begin{array}{}
x ∈ (A ∪ B)′ \text{ is equivalent to} \\
x ̸∈ A ∪ B \text{ is equivalent to} \\
¬(x ∈ A ∪ B) \text{ is equivalent to} \\
¬((x ∈ A) ∨ (x ∈ B)) \text{ is equivalent (by De Morgan laws in logic) to} \\
¬(x ∈ A) ∧ ¬(x ∈ B) \text{ is equivalent to} \\
(x ̸∈ A) ∧ (x ̸∈ B) \text{ is equivalent to} \\
(x ∈ A′ ) ∧ (x ∈ B′ ) \text{ is equivalent to} \\
x ∈ A′ ∩ B′
\end{array}
$$

### Cartesian product of sets
Definition: For two sets A and B, the set $A \times B = \{(x,y) | (x \in A) \wedge (y \in B)\}$ is called their Cartesian  product. 
E.x. $$\begin{array}{} 
A = \{x_1,x_2\},B = \{y_1,y_2\} \\
A \times B = \{(x_1,y_1),(x_1,y_2),(x_2,y_1),(x_2,y_2)\} \\
\end{array}$$

E.x.2.  If $A = \{x| \text{ x is real number }, 0 ≤ x ≤ 1 \}, B = \{x| \text{ x is real number}, 1 ≤ x ≤ 2 \}$, then $A × B$ can be represented as a rectangle on the plane with vertices in points with coordinates: $(0, 1), (0, 2), (1, 1), (1, 2)$. 

### Sets of Sets
Sets can server as elements of ther sets. e.g. 
1. $\{\{\emptyset\} , \{a\}, \{b\},\{a,b\} \}$ 
2. $\{\emptyset\}$   --> this a set containing an empty set
3. $\{\emptyset, \{\emptyset\}\}$ 

### Power Set
Definition: Let A be a set. Then $\{ B | B \subset A \}$ is called power set and is denoted by $2^A$. 
Examples: 
	- $2^\emptyset$ = $\{ \emptyset \}$ 
	- $2^{\{a\}} = \{ \emptyset, \{a\}\}$
	- $2^{\{a,b\}} = \{ \emptyset, \{a\},\{b\},\{a,b\}\}$
	- $2^{\{a,b\}} =  2^{\{a,b\}} \cup \{\{c\},\{c,a\},\{c,b\},\{c,a,b\}\}$

### Cardinality 
Let $A$ be a finite set of containing $n$ elements. The $n$ is called $cardinality$ of A. $n = |A|$. 
###### Theorem: $|A \cup B| = |A| + |B| - |A\cap B|$ 
Proof: Let's count elements from $A$ and then from $B$. So each element from $A\cup B$ will be counted at least once. Elements from $A \cap B$ will be counted twice. All other elements $(A \cup B) \setminus (A \cap B)$ are counted at least once. The formula follows. 

###### Theorem: $|A \times B| = |A||B|$ 
Proof: $|A \times B|$ is the set of all pairs $(x, y)$, where $x \in A, y \in B$.  For each of $|A|$ elements $x ∈ A$ there exist exactly $|B|$ pairs of the kind $(x, y)$ from $A \times B$. It follows that the total number of pairs (elements) in $A \times B$ is $|A||B$|.

###### Theorem: $|2^A| = 2^{|A|}$  
Proof: Let $A = \{a_1,a_2 . . . , a_n\}$. For a subset B of A, there are two contrary possibilities: $a_1 \in B$ or $a_1 \notin B$. The same is true for element $a_2$, hence there are $2 × 2 = 2^2 = 4$. Continuing this, we conclude that there are $2^n = 2^{|A|}$ possibilities for inclusion/exclusion of elements $a_1, a_2, . . . , a_n$ in $B$. Each of the possibilities gives a different subset B of A.

### Cardinality of sets
Links to [[Functions (maps)]]

Definition: A and B have the same cardinality if there exists bijective map $f: A \to B, f: B \to A$   
Going from even to to odd number; $x \mapsto x+1$; the map is bijective. 

A has "smaller" cardinality than set B if $A \subset B$ and $|A| \ne |B|$. 