# DM Problem S 1 - OG's work
---
*Date :* 20-09-2023
*Module :* #CM12004DM 
*Teacher*:  
*Resources :*

---

[[Problem sheet 1.pdf|Questions]] 
# Problem Sheet 1

1. I)  $P = X ∨ Y , Q = ¬(X ∧ Y )$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \vee Y && Q=\neg(X \wedge Y) && P\rightarrow Q \\
\hline
T && T && T && F && F \\
T && F && T && T && T \\
F && T && T && T && T \\
F && F && F && T && T \\
\hline
\end{array}
$$
It is **neither** tautology or identically false.

II) $P = X ∨ Y , Q = ¬X ∧ ¬Y$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \vee Y && Q=\neg X \wedge \neg Y && P\rightarrow Q \\
\hline
T && T && T && F && F \\
T && F && T && F && F \\
F && T && T && F && F \\
F && F && F && T && T \\
\hline
\end{array}
$$
It is **neither** tautology or identically false. 

III) $P = X → Y , Q = (¬X ∨ Y ) ∧ (¬X ∨ X)$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \rightarrow Y && Q=(\neg X \vee Y) \wedge (\neg X \vee X) && P\rightarrow Q \\
\hline
T && T && T && T && T \\
T && F && F && F && T \\
F && T && T && T && T \\
F && F && T && T && T \\
\hline
\end{array}
$$
Sincel all the values of $P\rightarrow Q$ are True int the truth table above we can confirm that it is a **Tautology**. 

IV) $P = X → ¬Y , Q = Y → ¬X$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \rightarrow \neg Y && Q= Y \rightarrow \neg X && P\rightarrow Q \\
\hline
T && T && F && F && T \\
T && F && T && T && T \\
F && T && T && T && T \\
F && F && T && T && T \\
\hline
\end{array}
$$
Sincel all the values of $P\rightarrow Q$ are True int the truth table above we can confirm that it is a **Tautology**. 

V) $P = X ∧ (Y ∨ Z), Q = (X ∨ Y ) ∧ (X ∨ Z)$
$$
\begin{array}{|c c c|}
\hline
X && Y && Z && P= X \wedge (Y \vee Z) && Q= (X \vee Y) \wedge (X \vee Z) && P\rightarrow Q \\
\hline
T && T && T && F && F && T \\
T && T && F && F && F && T \\
T && F && T && F && F && T \\
T && F && F && F && T && T \\
F && T && T && F && T && T \\
F && T && F && T && T && T \\
F && F && T && T && T && T \\
F && F && F && T && T && T \\
\hline
\end{array}
$$
Sincel all the values of $P\rightarrow Q$ are True int the truth table above we can confirm that it is a **Tautology**. 

VI) $P = X → Y , Q = ¬X → ¬Y$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \rightarrow Y && Q=(\neg X \rightarrow \neg Y) && P\rightarrow Q \\
\hline
T && T && T && T && T \\
T && F && F && T && T \\
F && T && T && F && F \\
F && F && T && T && T \\
\hline
\end{array}
$$
It is **neither** tautology or identically false.

VII) $P = X → Y , Q = ¬(Y → X)$
$$
\begin{array}{|c c c|}
\hline
X && Y && P=X \rightarrow Y && Q= \neg(Y \rightarrow X) && P\rightarrow Q \\
\hline
T && T && T && F && F \\
T && F && F && F && T \\
F && T && T && T && T \\
F && F && T && F && F \\
\hline
\end{array}
$$
It is **neither** tautology or identically false.

VIII) $P = (X → Y ) ∧ (Y → Z), Q = X → Z$ 
$$
\begin{array}{|c c c|}
\hline
X && Y && Z && P= (X \rightarrow Y) \wedge (Y \rightarrow Z) && Q= (X \rightarrow Z) && P\rightarrow Q \\
\hline
T && T && T && T && T && T \\
T && T && F && F && F && T \\
T && F && T && F && T && T \\
T && F && F && F && F && T \\
F && T && T && T && T && T \\
F && T && F && F && T && T \\
F && F && T && T && T && T \\
F && F && F && T && T &&  T\\
\hline
\end{array}
$$
Sincel all the values of $P\rightarrow Q$ are True int the truth table above we can confirm that it is a **Tautology**.


2. a) There are 16 binary logical connectives. 
	
	b) Express XOR via  I) $\neg$ , $\wedge$ 
	$$
	\begin{array}{|}
	\hline
	X && Y && X \vee Y && \neg (X \wedge Y) && (X\vee Y) \wedge  \neg (X \wedge Y) && X \text{ XOR } Y \\ 
	\hline
	T && T && T && F && F && F \\
	T && F && T && T && T && T \\
	F && T && T && T && T && T \\
	F && F && F && T && F && F \\
	\hline
	\end{array}
	$$
	So by comparing values in the truth table we can say that: $X \text{  XOR  } Y \equiv (X\vee Y) \wedge  \neg (X \wedge Y)$. Hence 
	$$ 
	\begin{array}{}
	\neg \neg (X \vee Y) \wedge \neg (X \wedge Y) \\
	\therefore \neg (\neg X \wedge \neg Y) \wedge \neg(X \wedge Y )
	\end{array}
	$$

	II) $\neg , \vee$
	$$
	\begin{array}{} 
	(X \vee Y ) \wedge (\neg X \vee \neg Y) \\
	\neg \neg ((X \vee Y ) \wedge (\neg X \vee \neg Y)) \\
	\neg (\neg (X \vee Y ) \vee \neg (\neg X \vee \neg Y))
	\end{array}
	$$

	III) $\neg, \rightarrow$ 
	$$ 
	\begin{array}{}
	\neg(\neg X \vee Y) \vee \neg(\neg Y \vee X) \\
	(X \rightarrow Y) \rightarrow \neg(Y \rightarrow X)\\
	\end{array} $$
	c) NOR is defined as: $X \text{ NOR } Y ≡ ¬(X ∨ Y )$ .
	Express each of connectives below via only NOR.
	I) **∧**
	$$
	\begin{array}{}
	X \wedge Y = \neg \neg (X \wedge Y) \\
	= \neg(\neg X \vee \neg Y) \\
	= \neg((X\:NOR \: Y)\vee(Y\:NOR\:Y)) \\
	= (X \: NOR \: X)\: NOR \:(Y \: NOR \: Y)\\
	\end{array} $$
  II) **∨**
	  $$
	\begin{array}{}
	X \vee Y = \neg \neg (X \vee Y) \\
	= \neg(X \: NOR \: Y) \\
	= (X \: NOR \: Y)\: NOR \:(X \: NOR \: Y)\\
	\end{array} $$
  III) **→**
	$$
	\begin{array}{}
	X \rightarrow Y = \neg X \vee Y\\
	= \neg \neg (\neg X \vee Y)\\
	= \neg (\neg X \: NOR \: Y) \\
	= \neg ((X \: NOR \: X)\: NOR \: Y) \\
	= ((X \: NOR \: X) \: NOR \: Y \:) \: NOR \: ((X \: NOR \: X) \: NOR \: Y \:)
	\end{array} $$
  IV) **¬**
	$$ \neg X = X \: Nor \: X $$
3. a)
	I) $∀x ∈ Z∃y ∈ Z(x^2 < y + 1)$
		This is a **True** Statement. If we let $y = x^2$ the statement is true for all values of x in Z. 
	
	II) $∃x ∈ Z∀y ∈ Z(x^2 < y + 1)$
		If we let $y = x^2 -1$ then $x^2 < (x^2 -1) + 1$ which is a contradictory statement. Hence it is **False**. 
	
	III) $∃y ∈ Z∀x ∈ Z(x^2 < y + 1)$
		**False** Statement. If $x^2 -1 < y$. We know $x^2 \ge 0$  so if $y = 0$ statement is false. 
	
	IV) $∀x ∈ Z∃y ∈ Z((x < y) → (x^2 < y^2 ))$
		**True** Statement. 

	b)
	I).  Prove that the statement $∀x∈Z \ ∀y ∈ Z(x^2 < y + 1)$ is false by giving an example of integers x and y disproving it.
	$$ \begin{array}{}
	Let \ x = -4 \ and \ y =4 \\
	x^2 = 16; \ y+1 = 5; \\
	Hence \ x^2 \nless y+1 \\
	\end{array}$$
	II) Prove that the statement $∃x ∈ Z \ ∃y ∈ Z(x^2 < y + 1)$ is true by giving an example of integers x and y proving it.
	$$ \begin{array}{}
	Let \ y = x^2 \\
	So, \ x^2 < x^2 + 1\\
	let x = 5 \ then \ y = 25 \\
	Hence \ 5^2 < 25+1
	\end{array} $$
	III) Prove that the statement $∀y ∈ Z∃x ∈ Z(x^2 < y + 1)$ is false by giving an example of an integer y disproving it.
	$$
	\begin{array}{}
	We \ know \ x^2 \ge 0\\
	Let \ y = -5 \\
	Then \ x^2 \nless -5 + 1. \\ \text{So the statement is false. }
	\end{array}
	$$
	IV) Prove that the statement $∃x ∈ Z∀y ∈ Z((x < y) → (x^2 < y^2 ))$ is true by giving an example of an integer $x$ proving it.
 $$\begin{array}{}
 \text{It's known that: } x^2 \ge 0 \\
 \text{ Let x = y-1}\\
 \text{The statement becomes true for all values of y; ie;}\\
 ((y-1) < (y)) \to \ ((y-1)^2 < (y^2))\\
 \text{Let y = 5 then x = 4}\\
 \text{4 < 5} \to 16 < 25
 \end{array}$$

4, Let A = {a, b, c}, B = {a, b}, C = {a, c}, D = {b, c}, E = {a}, F = {b}, G = {c}, H = ∅. Simplify the following expressions; in each case answer should be one of these sets.
	I) $B ∪ C ∪ D$
$$ \begin{array}{} 
	\{a,b\} \cup \{a,c\} \cup \{b,c\} \\
	\{a,b,c\} \cup \{b,c\}\\
	\{a,b,c\}\\
	\therefore \text{Set A}
	\end{array} $$
II) $B ∪ C$
$$\begin{array}{} 
\{a,b\} \cup \{a,c\} \\
\{a,b,c\}\\
\therefore \text{Set A} \\
\end{array}$$
III) $B \cap C \cap D$
$$\begin{array}{} 
\{a,b\} \cap \{a,c\} \cap \{b,c\} \\
\{a\} \cap \{b,c\}\\
\emptyset\\
\therefore \text{Set H} \\
\end{array}$$
IV) $G \setminus B$
$$\begin{array}{} 
\{c\} \setminus \{a,b\} \\
\{c\}\\
\therefore \text{Set G}
\end{array}$$
V) $D \setminus B$
$$\begin{array}{} 
\{b,c\} \setminus \{a,b\} \\
\{c\}\\
\therefore \text{Set G}
\end{array}$$
VI) $B \setminus A$ 
$$\begin{array}{} 
\{a,b\} \setminus \{a,b,c\} \\
\emptyset \\
\therefore \text{Set H}\\
\end{array}$$
VII) $(D \setminus G) \cup (G \setminus D)$
$$\begin{array}{}
(\{b,c\} \setminus \{c\}) \cup (\{c\} \setminus \{b,c\}) \\
\{b\} \cup \emptyset \\
\{b\}\\
\therefore \text{Set F}\\
\end{array}$$
VIII) $(B \setminus C) \setminus A$
$$\begin{array}{}
(\{a,b\} \setminus \{a,c\}) \setminus \{a,b,c\} \\
\{b\} \setminus \{a,b,c\} \\
\emptyset\\
\therefore \text{Set H}
\end{array}$$

5. a) Determine the cardinalities of the following sets;
	- $2^\emptyset = 2^0 = 1$
	- $2 ^ {\{0\}} = 2^{|\{0\}|} = 2^1 = 2$ 
	- $2 ^ {\{0\}\cup \{1\}} = 2^2 = 4$
	- $2^{\{0\} \cap \{1\}} = 1$ 
	- $2^{\{∅,0,1\}} = 8$
	- $2^{2^{2^{{\{0,1\}}}}} = 16^{\{0,1\}} =$  256
 
 b) Let $A = \{1,2,...,n\}.$ Determine the cardinalities of the following sets: 
 i) $\{(x, S)|x ∈ S, S ∈ 2^A\}$ 
	 $$ \begin{array}{}
	\{(x, S) | x \in A, x \in S, S \in 2^A \} \\
	2^A \setminus \{S | x \notin A, S \in 2^A \} \\
	2^A \setminus \{S |S \in 2^{A \setminus \{x\}}\} \\
	|\{S | S \in 2^A \} | = |2^A| = 2^n\\
	| 2^n \setminus 2^{A \setminus \{x\}}| \\
	2^n - 2^{|A| - |\{x\}|} \\
	2^n - 2^{n - 1} \\
	2 \times 2^{n-1} - 2^{n-1} \\
	2^{n-1} \\
	\therefore n \times 2^{n-1}
	\end{array}
	$$
ii) $\{S,T) | S \in 2^A, T \in 2^A, S \cap T = \emptyset \}$
**Hint**: Calculate the number of triples of pair-wise disjoint sets $(S, T, A \setminus (S \cup T))$ 

$$\begin{array}{}
A = (S \cap T) \cup (S \setminus (S \cap T)) \cup (T \setminus (S \cap T)) \cup (A \setminus (S \cup T)) \\
\text{So there are 3 options of sets for which a given element from A can be placed}\\
\text{Since there are 3 choices the cardinality of the above set is } 3^n

\end{array}
$$