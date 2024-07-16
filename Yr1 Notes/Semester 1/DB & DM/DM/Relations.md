# Relations
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :*  31-10-2023 
> > *Module :* #CM12004DM 
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Relations]]
> [[#Equivalence relations]]
> [[#Partition into equivalence classes]]
--- 

### Relations
Let $A, B$ be sets. A relation $R$ between $A \ and \  B$ is a subset of $A \times B$. In a special case of $A = B$, we say that $R \subset A \times A$ is a relation on $A$.
Examples:
	1. $A$ = set of students, $B$ = set of available teaching units. We define the relation $R \subset A \times B$ as $(x, y) \in R$ such that the student $x$ takes unit $y$.
	2. Any map $f : A \to B$ is a relation between A and B.
	3. $A = B = Z$. Define $R = \{(x,y) | x < y \}$. The notation $x < y$ is used instead of $(x,y) \in R$. 
	4. Let $A$ be a finite set. Any relation on $A$ can be interpreted as a directed graph. 
	![300](https://sites.google.com/a/cs.christuniversity.in/discrete-mathematics-lectures/_/rsrc/1409480658489/graphs/directed-and-undirected-graph/dir.png)

### Equivalence relations
$(x,y) \in R \equiv x * y$
**Definition:** A relation $∗$ on A is called an equivalence relation if:
	1. $∗$ is **reflexive**, i.e., for any $x \in A, x * x$
	2. $∗$ is **symmetric**, i.e., if $x ∗ y$, then $y ∗ x$
	3. $*$ is **transitive**, i.e., if $x ∗ y$ and $y ∗ z$, then $x ∗ z$ 

Ex. 
	1. = on $Z$
	2. Parity on $Z$ (means any two even are equivalent or any two odd are equivalent)
	3. $A =$ set of people, $x * y$ if they have the same birthday

**Definition:**. Let ∗ be an equivalence relation on a set A, let x ∈ A. The subset $[x] = \{y ∈ A| x ∗ y\}$ is called the equivalence class of the element $x$.
E.x. 
	- $=$ on $Z$, $n \in Z \ [n] = \{n \}$ 
	- Parity on Z: all even numbers are equivalent, as are all odd numbers.
	- Let A be a set of people. Define $x ∗ y$ as the predicate which is true if and only if $x$ has the same birthdate as $y$.

### Partition into equivalence classes
**Definition**: Lent $A$ be a finite set. Then a partition $A$ is a set of subsets of A: $A_1,A_2,...A_n$ of $A$ such that:
	a). $A = A_1 \cup A_2 \cup ... \cup A_n$
	b). $A_i \cap A_j = ∅$ for $i \ne j$.

When considering partition of any set. Let $A$ be any set (fininte or infinite). Then any set partition $P$ of $A$ is a subset of $2^A \setminus \emptyset$ such that sets in P are pairwise disjoint $(\cap = ∅)$ and their union is $A$. 

**Theorem**: Let $\ast$ be an equivalence relation on $A$. Then all distinct equivalence classes of elements in A form a partition of $A$. 
$Z = Z$, $Z = E \cup O$

---