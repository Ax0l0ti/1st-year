# Boolean Logic and Circuits
---
*Date :*  05-12-2023 
*Module :* #CM12002 
*Teacher*: #FabioNemetz 
*Resources :* [Introduction to Karnaugh Maps - YouTube](https://www.youtube.com/watch?v=RO5alU6PpSU&ab_channel=TheOrganicChemistryTutor), [Website for creating Sofp & k-maps](http://www.32x8.com/var4.html)

---
##### Contents: 
> [[#Standard Sum of Products (SofP)]]
> [[#Simplifying Formula]]
> [[#Karnaugh Maps]]
> 	[[#Creating K-maps from boolean formula]]
> 	[[#Creating formulas from K-maps]]
> 	[[#Application of K-maps]]
> 
--- 

There are two different kinds of circuits:
	- Combinational Logic
	- [[Sequential Logic]]

Combinational logic circuits combine their inputs in a a way that is:
	- Static
	- Deterministic (for each input combination there is a single output)
They are used to implement logic and arithmetic. 

Sequential logic circuits incorporate feedback from their outputs. They are
	•dynamic (changing over time), and can be
	•non-deterministic (several possible outputs for a given input).
They are used to implement "stateful" operations such as control circuits and memory cells. 

There are three fundamental logic operations:
	- AND
	- OR
	- NOT

De Morgan's laws 
$$
\begin{array}{}
\neg \neg A = A \text{ (double negation)} \\
\neg (A.B) = \neg A + \neg B \\
\neg (A+B) = \neg A . \neg B
\end{array}
$$

**XOR** operator is true only when one input (operand) is True. So True XOR True is False. 

Logic Gate Symbols
	![300](https://content.instructables.com/F09/9ZEY/IIHRJM27/F099ZEYIIHRJM27.png?auto=webp&frame=1&fit=bounds&md=b6cfc4e817d8619dfead8accac05371d)

![[Pasted image 20221205113625.png]]

There are two basic techniques for determining whether two formulas are equivalent:
	- Equational reasoning (by algebra)
	- Semantic reasoning (by truth tables)

Look at maths boolean logic for all the boolean logic rules

Question: Show that $A.(A + B ) = A$
	Answer: 		
		![[Binary Arithmetic Example 3.png]]
Question: Show that $A + A.B = A$
	Answer:
		![[Pasted image 20221205114257.png]]

### Standard Sum of Products (SofP)

A SofP of a Boolean formula is:
	- A series of terms joined by OR operation
	- Each term contains a combination of all variables joined by AND operation
	- e.g: $A + B.C = A.B.C + A.B.\neg C + A.\neg B . C + A.\neg B . \neg C + \neg A . B . C$

We arrived at the expression above by doing the following:
	![[Binary Arithmetic Example.png]]
	![[Boolean logic of Karnaugh maps.png]]
**Theorem**
Every boolean expression over $n$ variables is equivalent to a standard sum of products. 

### Simplifying Formula

Simplification of boolean algebra can be done in two stage proceses:
	1. First Convert the Boolean formula to a **standard sum of products**
	2. Then find the simplest form for this formula (the one with the fewest logic gates)

### Karnaugh Maps

###### Creating K-maps from boolean formula
For any formula, we can find the simplest equivalent **sum-of-products expression** using Karnaugh maps. These maps work well for up to 4 variables. 

The order when creating a K-map with always goes as such: $00,01,11,10$

*So here is how it goes. For a given formula you're filling in the value in the table. Once the table is created you're going to check variables and where that order fits in. Negation is always read as zero. Let's say we had ABC then the cell where A = 1, B=1 and C =1 is 1. Simiilarly, if $A \neg B$ then we fill the cell where A = 1 and B =0.*

So a boolean formula with four variables in a K-map will look as such:
![[Karnaugh maps Example 2.png]]

###### Creating formulas from K-maps
After the map is created any two adjacent squres with entries of 1 $\to$ corresponding product terms differ in only one variable. This means that one variable can be eleminated. 

Adjacent squres can be grouped in the powers of 2; ie, $2,4,8,...$. So more variables can be eliminated. Important to remember that when grouping variables they can be also be grouped around the edges. 

*So you read the map and see from the grouped variables which one's stay constant. The one's that change can be removed as they have no impact on the boolean formula. Look at the table below. Notice how the variables C and D keep changing as you go across the with the adjacent pairs. So they can be ignore. AB stays the same; its always 00. Since the value in the cells are 1 the boolean formula for the table becomes:* $\neg A \neg B$
![[Karnaugh maps Explanation.png]]
Look at more examples below for better understanding:
![[Karnaugh maps.png]]

*Simplifying Boolean expressions (recap)
1)  Write it in the form of a standard sum of products;
2)  Plot the product terms on a Karnaugh map;
3)  Find the smallest number of the biggest valid groupings that will encompass all of the marked squares (1s) of the Karnaugh map; and
4) Read off the function that results.*

### Application of K-maps

Sometimes certain combination of values of variables never occur. In these cases we don't need to consider some possible inputs because:
	- these inputs can't arise or
	- we don't need the output corresponding to them

We mark this with a letter 'x' or 'd' in the correspoinding squre of the map. When simplifying each 'x' can be treated as a 1 or 0, whichever leads to the simplest expression. 

For example a seven-segment display uses this idea. 
	- It is driven by binary coded decimal (BCD)
	- A separate set of combinational logic turns on or off each segment
![[Pasted image 20221212113528.png]]
![[Karnaugh maps Example.png]]
