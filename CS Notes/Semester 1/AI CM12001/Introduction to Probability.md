# Intro to Probability
---
*Date :* 09-02-2024
*Module :* #CM12001 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#Terminology]]
> [[#Notation]]
> [[# ]]
> 
--- 



--- 

### Basic terminology and notation  

#### Terminology
When dealing with uncertainty, we will use tools from **statistics** and **probability**. 

- A **statistic** is a quantity that summarises some data, such as the average daily sales of a newspaper or the frequency of a slot machine's payouts. 
- A **probability** is a value between zero and one that measures the chance of an uncertain event occurring, such as the chance of drawing a king from a pack of cards or the chance that it will rain tomorrow, given that it is sunny today.
- **Probability Distribution** is the distribution of all probabilities measured on a y axis of 0 to 1 
- Independent variables X does not affect Y and vice versa.

#### Notation

- basic probability 
	- $0 \leq p(\omega) \leq 1$
	- $\sum_\omega{p(\omega)}  = 1$
	- $p(X,Y)$ probability of $X$ **and** $Y$ 
- **given** - 
	- e.g Given Uni, i will kill myself  $p(death | university) = 1$
	- $p(a|b) = {{p(a \wedge b)}\over{p(b)}}$ hence $p(a|b) \times {p(b)} = {p(a \wedge b)}$
- **subset** $\phi$ of **sample space** $\Omega$ is called an **Event**
	- roll dice $\Omega = {[1,2,3,4,5,6]}$
	- an even dice roll gives $\phi = {[2,4,6]}$ 
- Basic laws
	- $p(a \wedge b) = p(a) + p(b) - p(a \vee b)$

