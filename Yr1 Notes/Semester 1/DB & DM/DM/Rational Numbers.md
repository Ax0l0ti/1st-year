# Rational Numbers
---
*Date :*  31-10-2023 
*Module :* #CM12004DM 
*Teacher*: 
*Resources :* [Introduction to Cauchy Sequences - YouTube](https://www.youtube.com/watch?v=jD5s2jvnH1k&ab_channel=ElliotNicholson)

---
##### Contents: 
> [[#Overview]]
> [[#Arithmetic operations on $Q$]]
> [[#Cauchy Sequences]]
> [[#Arithmetic of Cauchy sequence]]
> [[#Null Sequences]]
> [[#Equivalence relations for Cauchy sequences and real numbers]]
> [[#Real and Rational]]
--- 

# Overview

**Cauchy sequence** 
- terms in sequence begin to approach each other
- sequence around a number e.g $\pi$ sequence $= 3, 3.1, 3.12, 3.121, 3.1214$
- {$a_{n}$} + {$b_{n}$} = {$a_{n} + b_{n}$}
**Null sequence**
- sequence approaches 0 
- basically a Cauchy around 0 



Let $A = \{\frac{x}{y} | x,y \in Z, y \ne 0 \}$ then we can't say that $\frac{1}{2} \equiv \frac{27}{54}$. This is because $x$ and $y$ would be different integers from the set, hence they become different from each other even though their representation is the same. 
$\frac{x_1}{y_1} \text{is equivalent} \frac{x_2}{y_2}$ if and only if $x_1y_2 = x_2y_1$ 

>**Definition**: The set $Q$ of all rational numbers is the set of all equivalence classes of the relation $\sim$ on $A$. 

E.X. 
	The set $\{\frac{1}{2}, \frac{3}{6}, \frac{27}{54}, . . .\}$ consisting of all fractions of the kind $\frac{a}{2a}$ for all non-zero $a ∈ Z$ is an equivalence class of $\sim$ on A, hence this set is a rational number.

*So from my understanding, an equivalence class is a set containing fractions which are equivalent. This class in itself be called a rational number. Performing operation on any of the fraction from the class would result in another equivalent fraction.*

### Arithmetic operations on $Q$
$Q$ represents set of all rational numbers
**Definition** (arithmetic over fractions):  
	$$\frac{x_1}{y_1} + \frac{x_2}{y_2} \equiv \frac{x_1y_2 + x_2y_1}{y_1+y_2}$$
	$$\frac{x_1}{y_1} \times \frac{x_2}{y_2} \equiv \frac{x_1x_2}{y_1y_2}$$
>**Definition** (arithmetic over **Q**):
 *The ideas defined below also work for multiplication, i.e; pq*
 Let $p,q \in Q$ (*p, q are equivalence classes of **Q***). Then $p+q$ is defined as follows:
	Choose a fraction in $p \to \frac{x_1}{y_1}$
	Choose a fraction in $q \to \frac{x_2}{y_2}$
	then $p+q$ is defined as a rational number (*another class*) which contains the fraction $\frac{x_1}{y_1} + \frac{x_2}{y_2}$. 

**Theorem**: The result of an arithmetic operation over $Q$ does not depend on particular choices of fractions $\frac{x_1}{y_1}, \frac{x_2}{y_2}$.

**Proof**: $$\begin{array}{}
\frac{x}{y} ∼ \frac{x′}{y′} \ and \ \frac{z}{w} ∼ \frac{z ′}{w′} \ then \\\
\frac{x}{y} + \frac{z}{w} ∼ \frac{x′}{y′} + \frac{z′}{w′} \ and \ \frac{x}{y} + \frac{z}{w} ∼ \frac{x′}{y′} \cdot \frac{z′}{w′}
\end{array}$$



### Cauchy Sequences

Cauchy Sequences tend towards a point e.g $\sqrt{2}$
**Definition**: A sequence of rational numbers is a function $a: N \to Q$. 
Traditionally, the image  of $a$ at $n$ is denoted by $a_n$ and the whole sequence by $\{a_n\}$. One can think of a sequence as of an infinite string $a_1, a_2, . . . , a_n, . . ..$ We will refer to an as to the $nth$ member of the sequence ${a_n}$.

**Definition**: Sum and product of two sequences $\{a_n\}$ and $\{b_n\}$ are defined as follows: 
	- $\{a_n\} + \{b_n\} = \{a_n + b_n\}$
	- $\{a_n\} · \{b_n\} = \{a_nb_n\}$ 
	- $\{a_n\} - \{b_n\} = \{a_n\} + \{-b_n\}$ 

For any two numbers $x,y$ the absolute values $|x + y| \le |x| + |y|$ and $|x − y| ≤ |x| + |y|$

>**Definition**: A sequence ${a_n}$ of rational numbers is called **Cauchy sequence** when the following condition is satisfied. For every rational $\epsilon > 0$ there exists $N \in N$ such that for any two natural numbers $n, m \ge N$ we have $|a_n − a_m| < \epsilon$.
>
>Just means a sequence whose elements become arbitrarily close to each other as the sequence progresses.

![200](https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Cauchy_sequence_illustration.svg/375px-Cauchy_sequence_illustration.svg.png)

### Arithmetic of Cauchy sequence
**Theorem**: If $\{a_n\}$ and $\{b_n\}$ are Cauchy sequences, then $\{a_n\}+\{b_n\}$ and $\{a_n\} · \{b_n\}$ are also Cauchy sequences.

**Proof**: 


### Null Sequences
>**Definition**: A null sequence is a sequence $\{a_n\}$ of rational numbers with the following property. For any rational number $\epsilon > 0$ there exists a natural number N such that if a natural number $n \ge N$, then $|a_n| < \epsilon$.

Example: 
	The sequence $\{a_n\}$ where $a_n$ = $\frac{1}{n}$ is a null sequence (for a given $ε$ take $1/ε + 1$ as N).

**Theorem**: Any null sequence $\{a_n\}$ is a Cauchy sequence. 
**Proof**: 


### Equivalence relations for Cauchy sequences and real numbers
Let C be the set of all Cauchy sequences. 
Introduce the following relation ∼ on C. For $\{a_n\}, \{b_n\} \in C$ let $\{a_n\} ∼ \{b_n\}$ if the difference $\{a_n\} − \{b_n\}$ is a null sequence.
Example: $\{1/n\} ∼ \{1/n^2\}$ 


### Rational & Irrational Proof

$\mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$

using a square size 1 x 1, cross from corner to corner is $\sqrt{2}$ 

Suppose $\sqrt{2}  =$ $x/y$ ==simplified== $\implies 2 = x^2 / y^2 \implies 2y^2 = x^2 \implies x^2$ is even $\implies x is even \implies x = 2z \implies 2y^2 = 4z^2 \implies y^2 = 2z^2 \implies y = even$
==CONTRADICTION==
$x/y$ is simplified yet $y$ is even $\vee$ $x$ is even

### Irrational Approximation



