# Finite Automata & Regular Languages
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  03-10-2024
> > *Module :* [[Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Finite Automata & Regular Languages]]
> [[#Deterministic finite automata]]
> [[#Formal Defintion of when DFA accepts]]
> [[#Regular Language]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  An **alphabet** $\Sigma$ is afinte nonempty set of Symbols 
> $b)$ - A **word** $w$ over alphabet $\Sigma$ is a finite (possible empty) sequence of $\Sigma$ 
> $c)$ - Set of **All Words** $= \Sigma^*$ (all might not make sense e.g english & waddfgle)
> $d)$ - Any subset $L ⊆ \Sigma^*$ is called a **language** over $\Sigma$.
> $e)$ - $e$ denotes the **==Empty word==** (also shown as $\epsilon$)
> $f)$ - w denotes the **length** of a word
> > >[!abstract]+ NFA vs DFA
> > All $DFA \gg NFA$, But $NFA \not\gg DFA$
> > DFA, 1 input 1 action 
> > NFA, 1/0 input many actions 
> > 

---
## Detirministic finite automata: 

Loads of Finite Automata, 
some Deterministic -  input = guaranteed output
some non-deterministic -  input = P(outputs) 

> [!info] DFA
> A **deterministic finite automaton**, or DFA, consists of **==five==** objects $(Q,Σ,δ,s,F)$, where: 
> - $Q$ is a finite set of **states**.
> - $Σ$ is an **alphabet**.
> - $δ:Q×Σ→Q$ is the **transition function**. 
> - $s ∈Q$ is the **initial state**. 
> - $F ⊆Q$ is the set of **accepting states**.
> > [!Example]+ DFA Formal Defintion Example
>  ![[Example DFA formal definition.png|400]]

## Formal Definition of when DFA accepts
>[!success]
 >Definition Let $A = (Q,Σ,δ,s,F)$ be a deterministic finite automaton, and $w =a_1...a_n$ a word in $Σ∗$. We say that A accepts $w$ if there exists a sequence of states $r0,...,rn ∈ Q$ such that: 
> 1. $r0 = s$,
 >2. $δ(r_i,a_{i+1}) = r_{i+1}$ for $i = 0,...,n − 1$,
 >3. $r_n ∈ F$

## Non-deterministic Finite Automaton

> [!info] NFA
> A **Non-determanistic finite automaton**, or DFA, consists of **==five==** objects $(Q,Σ,δ,s,F)$, where: 
> - $Q$ is a finite set of **states**.
> - $Σ$ is an **alphabet**.
> - $\Delta\subset Q \times (Q×Σ→Q$ is the **transition ==relation==**. #TODO 
> - $s ∈Q$ is the **initial state**. 
> - $F ⊆Q$ is the set of **accepting states**.
> > [!Example]+ DFA Formal Defintion Example
>  ![[Example DFA formal definition.png|400]]

## Regular Language

Definition Let $A = (Q,Σ,δ,s,F)$ be a **DFA**. 
Then the language $L(A) ⊆ Σ^∗$ is defined by $L(A) = \{w ∈ Σ∗|A\text{ accepts }w\}$ 
Definition (Regular language) 
A language $L ⊆ Σ^∗$ is called regular if there exists a DFA $A$ such that $L =L(A)$

