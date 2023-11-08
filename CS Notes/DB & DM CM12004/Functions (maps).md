# Functions (maps)
---
*Date :* 24-10-2023 
*Module :* #CM12004DM 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#Surjective maps]]
> [[#Injective maps]]
> [[#Bijective maps]]
> [[#Inverse Maps]]
> [[#Composition of Maps]]
--- 

**Definition:** If $f : A → B$, then A is called the domain of $f$, B is called the range (or co-domain). If $x \mapsto y$, then $y$ is called the image of $x$, $x$ is called the pre-image of $y$, $x$ is also called the argument of $f$. We say that $f$ carries $x$ to $y$. 

If the range $B$ of a map f is a set of numbers, then $f$ is often called a function. However, the term function is also sometimes used as a synonym for map.

Examples:
	1. A computer program. $A$ is the set of all possible inputs on which the program terminates, $B$ is the set of all possible outputs. 
	2. $f : Z \rightarrow Z$, such that to $x \in Z$ the map $f$ relates $x^2 \in Z$. The latter condition is usually written as $x \mapsto x^2$, or as $f(x) = x^2$. 
	3. Let $A$ be a set of students taking a certain exam, $B$ be a set of all possible marks, e.g. $B = \{0, 1, 2, . . . , 100\}$. Then the exam is a map from A to B.

There are two **important** conditions required for it to be considered a map: 
	1. Every $x ∈ A$ is “used”, i.e., $x$ is an argument to which a certain image $y ∈ B$ corresponds; 
	2. To every $x ∈ A$ corresponds only one image from $B$.
	![200](https://upload.wikimedia.org/wikipedia/commons/thumb/d/df/Function_color_example_3.svg/1200px-Function_color_example_3.svg.png)

Example: List all four possible maps from $A = \{x_1,x_2\} \ to \ B = \{y_1,y_2\}$
	$$\begin{array}{}
	f_1(x_1) = y_1, f_1(x_2) = y_2; \\
	f_2(x_1) = y_2, f_2(x_2) = y_1; \\
	f_3(x_1) = y_1, f_3(x_2) = y_1; \\
	f_4(x_1) = y_2, f_4(x_2) = y_2 \\ 
	\end{array}
	$$
Definition: **Identity map** on a set A is defined as $I_A : A \rightarrow A$ such that $x \mapsto x$. 
So what we are saying is that the map has "A" as both the domain and the range. 

### Surjective maps (onto)
Definition: A map $f: A \rightarrow B$ is called surjective if $\forall y \in B \exists x \in A(f(x) = y)$. This means that in surjective map, every element from the range has a pre-image / every element in the domain is used. 
![300](https://www.researchgate.net/publication/342801379/figure/fig1/AS:911228998279169@1594265331655/Graphical-representation-of-injective-and-surjective-functionals.png)
Examples:
	1. The map from the set of all humans to the set of all human mothers is surjective (each mother, by the definition, has a child).
	2. Let A = set of all UK university students, B = set of all UK universities $f: A \to B$ 
	3. The identity map is surjective. 
	4. $x \mapsto x_2$ is not surjective (e.g., −1 has no pre-image). However, over complex numbers, $f(x) = x_2$ is surjective.
	5. $f(x) = x^3$ is surjective over real numbers. 

### Injective maps (one to one)
Definition: A map f : A → B is called injective if $\forall x_1 \in A\forall x_2 \in A((x_1 \ne x_2) \to (f(x_1) \ne f(x_2))$ 
So simply, two different arguments have two different images. i.e. "different x maps to different y"
Examples: 
	- $f(x) = x^2$ is not injective
	- $f(x) = 2^x$ is injective

### Bijective maps (One-One onto)
Definition: A map $f: A \to B$ which is both surjective and injective is called bijective. 
Example:
	- $I_A$(identity map) is bijective
	- $f(x) = x^3$ is bijective $\to$ because its one to one and every y has a x value

### Inverse Maps
Definition: Let $f: A \to B$ be a map. Map $f^{-1}: B \to A$ is called inverse of $f$ if $f(x) = y$ is equivalent to $f^{-1}(y): = x$. 

**Theorem:** A map $f : A \to B$ has an inverse if and only if $f$ is bijective. 
**Proof:** Assume $f$ has an inverse. Then for $y \in B$ there is $x \in A$ such that $f^{-1}(y) = x$ which is equivalent to $y = f(x)$. This means $y = f(x)$ is surjective. Can't be two $x_1 = f^{-1}(y)$ and $x_2 = f^{-1}(y) (x_1 \ne x_2)$ 
equivalent $y = f(x_1), y = f(x_2)$ Thus $f$ is injective. 

### Composition of Maps
Definition: $f: A \to B , g: B \to C$
composition of $f$ and $g$ is map: $g \circ f: A \to C$ such that $g \circ f(x) = g(f(x))$ . 

Example: 
	$f(x) = x+1, g(y) = y^2$ 
	so, $g \circ f(x) = (x + 1)^2$ and $f \circ g(y) = y^2 + 1$ 

**Theorem:**
	1. The composition of two injective maps is injective.
	2. The composition of two surjecrjective.
**Proof:**
	Let both maps $f: A \to B$, $g: B \to C$ be injective. Let $x_1,x_2 \in A$ and $x_1 \ne x_2$. Then function $f(x_1) \ne f(x_2)$ is injective. Then $g(f(x_1)) \ne g(f(x_2))$ since $g$ is injective. Hence, $g \circ f(x_1) \ne g \circ f(x_2)$, which means $g \circ f$ is injective. 

### Inverse map and identity map
Let $f : A \to B$ be a bijective map. 
Let $I_A : A → A$ and $I_B : B → B$ be the identity map.
**Theorem:** Composition $f \circ f^{−1}$ coincides with the identity map $I_B$; composition $f^{−1} \circ f$ coincides with the identity map $I_A$.

**Theorem:** Each of the composition $I_B \circ f$ and $f \circ I_A$ coincides with f. 

### Map as a subset of Cartesian Product
**Definition**: A map $f: A \to B$ is a subset of $A \times B$ such that for every $x \in A$ there exists one and only $y \in B$ with $(x,y)\in f$. 
E.x. $f(x) = x^2$ the above definition describes their graphs. 










