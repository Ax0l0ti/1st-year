# DM Problem S 2 - OG's work
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :* 20-09-2023
> > *Module :* #CM12004DM 
> > *Teacher*:  
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic

---
[[Problem sheet 2.pdf|Questions ]]

1. 
	I) $3^2 = 9$
	II) $\frac{3!}{(3-2)!} = 6$
	III) $0$
	IV) $2^3 = 8$
	V) $2^3 - {2\choose 1 }\cdot 1^3 = 6$
2. 
	I) Let $\ x \in N$, then $f(x) = x^3$ is a bijective map. 
	
	II) Let $E = \text{Set of all even numbers}$. Then for all $x \in E, f(x) = x+1$ is a bijective map from even to odd.  
	
	III) Let $x \in N$.  Given $x$ is even, then $\frac{x}{2}$ will result in positive integer. Given $x$ is odd, then $\frac{-x+1}{2}$ will result in negative integer. Hence there is a surjection from $N$ to $Z$. 
	$$\begin{equation*}
	f(x)=\begin{cases}
    \frac{x}{2} \quad &\text{if} \, x \text{ is even} \\
    -2x+1 \quad &\text{if} \, x \text{ is odd}  \\
     \end{cases}
	\end{equation*}$$
	
	IV) Let $x \in Z$, then for all positive $x$, $2x$ will result in positive evens. Similary for all negative $x$, $-2x+1$ will result in positive odds. Hence all $x \in Z$ map to elements in $N$. 
	$$\begin{equation*}
	f(x)=\begin{cases}
	          2x \quad &\text{if} \, x>0 \\
	          -2x+1 \quad &\text{if} \, x<0  \\
	     \end{cases}
	\end{equation*}$$

3. 
	I) $R = \{(x, y)| x = y + 2 \}$
	$$\begin{array}{}
	(x , y = x-2) \\
	(x,x-2)\\
	\therefore f(x) = x-2
	\end{array}
	$$
	It's a linear map. So every domain maps to exactly one element in the range.  It is a **map from Z to Z**.

	II) $R = \{(x, y)| x = y^2 \}$
	$$\begin{array}{}
	(x,y=\sqrt{x}) \\
	(x,\sqrt{x}) \\
	\therefore f(x) = \sqrt{x}
	\end{array}
	$$
	**Not a map from Z to Z**. If we let $x=2$, relation doesn't map to an integer. 

	III) $R = \{(x, y)| x^2 = y \}$
	$$\begin{array}{}
	(x,x^2) \\
	\therefore f(x) = x^2 \\
	\end{array}
	$$
	**It is a map from Z to Z**. Assigning any integer value to $x$ will always result in an integer value. Every domain value maps to a single range value. 

	IV)  $R = \{ (x, y)| x = \frac{y^{\frac{1}{3}}} {2} \}$
	$$\begin{array}{}
	(x,2x = y^{\frac{1}{3}}) \\
	(x,y=8x^3) \\
	(x,8x^3) \\
	\therefore f(x) = 8x^3 \\
	\end{array}
	$$
	**It is a map from Z to Z**. Assigning any integer value to $x$ will always result in an integer value. Every domain value corresponds to a single image. 

4. 
	I) $x + y$ is an odd integer
	It is a **symmetric relation**. $$x+y = (2a -1) =  y+x$$
	Not Reflexive relation because: $x + x = 2x$ which is not odd integer. 

	Not transitive because if $x+y$ is odd and $y+z$ is odd then $x+z$ can be an even number. 
	
	II) $x+y$ is an even number
	It is a **Reflexive relation** $$x + x = 2x$$As $x+x$ is even we can say that $x \ast x$. The relation $\ast$ is seen to be reflexive.
	
	It is a **symmetric relation** because if : 
	$$x+y = 2a \ then \ y+x = 2a$$
	It is a **transitive relation** as if $x+y$ is even and $y+z$ is even then $x+z$ is even. 
	$$\begin{array}{}
	x + y = 2a, \ y+z = 2b\\
	(x+y)+(y+z) = 2a + 2b\\
	x + z = 2a + 2b - 2y\\
	x + z = 2(a+b - y) \end{array} $$
	III) $xy$ is an odd integer
	For a product to be an odd integer both the multipliers $(x \ and \ y)$ must be odd. 
	It is a **reflexive relation** as: $$\text{As x is odd, } x \times x = odd \ integer$$
	It is a **symmetric relation** because: $$ xy = yx$$
	It is a **transitive relation**. If $x\times y = odd$ and $y \times z = odd$ then $x \times z = odd$. 
	
	IV) $x + xy$ is an even integer
	It is a **Reflexive Relation** because $x + x^2$ is always even whether $x$ is assigned to be an even or odd integer .
	$$\begin{array}{} x + x \times x = x+x^2 \\ \end{array} $$
	It is a **Transitive Relation**. The state of $x+xy$ being even is decided by the value assigned to $x$. Similarly value of $y$ decides if  $y+yz$ is even. So if $x+xy$ is even and $y+yz$ is even then $x + xz$ will be even.  

	It is not symmetric relation because if $x+xy$ is even then it is not necessary that $y+yx$ is even. If we assign an odd integer to $y$ and an even integer to $x$, $y+yx$ is odd whereas $x+xy$ is even. 

1. Consider the subset relation $⊂$ on the set $A$ = {{b}, {c}, {a, b}, {a, c}, {a, b, c}}
	
	$a)$ Is ⊂ a partial order on $A$, a strict partial order on A, or neither? Justify your answer
	- Every element $x \in A$ is a subset of itself. Hence $x \subset x$. It is reflexive. 
	- We don't have$(x,y)$ and $(y,x)$ for all $x,y \in A$, so it is anti-symmetric.
	- $\{a,b\} and \{a,c\} \to \{a,b,c\}$ hence it is transitive. 
	
		It is a **Partial order** on $A$. 

	$b)$ Is $⊂$ a total order on $A$? Justify your answer
	- Firstly it is a pratial order set. 
	- To be a total order $\forall (x,y) \in A$ either $x\subset y$ or $y \subset x$. This is False with the elements in $A$. 
		Hence it is a **Not a Total Order Set**. 

	$c)$ Decide whether there are maximal elements, and whether there are minimal elements, in $A$ with respect to $⊂$. If such elements exist, list them all.
		$$ \begin{array}{} 
		\{b\} \text{is a subset of} \{a,b\}  \text{and} \\
		 \{c\} \text{is a subset of} \{a,c\} \text{ and } \\ 
		 \{a,b\} \text{ and } \{a,c\} \text{are a subset of }\{a,b,c\}
		 \end{array}$$ 
	- $\{a,b,c\}$ is a maximal. 
	- $\{b\}$, $\{c\}$ is a minimal.