# FSM Turing Machines
---
*Date :* 15-11-2023
*Module :* 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]]  [[#ChatGPT notes]]
> [[#1. Definition]]
> [[#2. Components of FSM]]
> [[#3. Types of FSM]]
> [[#4. State Transition Diagram]]
> [[#5. Mealy and Moore Machines]]
> [[#6. Turing Machines]]
> [[#7. Applications of Turing Machines]]
> [[#8. Limitations of FSM and Turing Machines]]
> [[#9. Formal Representation]]
> [[#10. Extended Models]]
> 
--- 

==the transition function δ is key:== ${– Q × Γ → Q × Γ × \{L, S, R\} }$
	A machine is in a state $q ∈ Q$ and the head is over the tape at symbol $a ∈ Γ$, then after the move we are in a state $r ∈ Q$ with $b ∈ Γ$ replacing the a on the tape and the head has moved either left (L), Stay/Stop (S) or right (R)
	
e.g $δ \space q0 \times a → q1 \times b \times L$

## ChatGPT notes 

### Finite State Machines (FSM) and Turing Machines:

##### 1. Definition:

- A Finite State Machine (FSM) is a computational model used to design and represent systems with discrete states and transitions.
- Turing Machines are a specific type of FSM that extends the concept to include an infinite tape for data storage.

##### 2. Components of FSM:

- **States (Q):** Distinct conditions or situations that the system can be in.
- **Transitions (Δ):** Rules defining the change from one state to another based on input conditions.
- **Inputs (Σ):** External stimuli that trigger state transitions.
- **Outputs (Λ):** Response or actions produced by the system as a result of state transitions.

##### 3. Types of FSM:

- **Deterministic Finite Automaton (DFA):**
    - Each input leads to a unique next state.
    - Well-defined and predictable behavior.

- **Nondeterministic Finite Automaton (NFA):** 
    - Multiple possible next states for a given input.
    - Useful in certain theoretical applications.

##### 4. State Transition Diagram:

- Graphical representation of FSM using circles (states) and arrows (transitions).
- Each state is labeled, and transitions are annotated with input conditions.

##### 5. Mealy and Moore Machines:

- **Mealy Machine:**
    
    - Outputs depend on both the current state and input.
    - Output is associated with transitions.
- **Moore Machine:**
    
    - Outputs depend only on the current state.
    - Output is associated with states.

##### 6. Turing Machines:

- Turing Machines are a more powerful computational model than FSM.
- Consists of an infinite tape, a read/write head, and a finite set of states.
- Can simulate the logic of any algorithm and solve problems that FSMs cannot.

##### 7. Applications of Turing Machines:

- Used in theoretical computer science to define the limits of what can be computed algorithmically.
- Turing completeness is a criterion for determining if a system can perform any computation.

##### 8. Limitations of FSM and Turing Machines:

- FSMs are suitable for systems with a finite number of states and discrete transitions.
- Turing Machines are powerful but have limitations in solving undecidable problems.

##### 9. Formal Representation:

- **State Table:** Tabular representation of states, inputs, outputs, and transitions.
- **State Transition Equation:** Mathematical representation defining state transitions.

##### 10. Extended Models:

- **Hierarchical FSMs:** Organizing states into hierarchies for better organization and management.
- **Extended FSMs (EFSM):** Including additional features like counters and timers.

 Finite State Machines and Turing Machines are fundamental concepts in theoretical computer science. Understanding their properties and applications is crucial for a comprehensive grasp of the limits and capabilities of computation.
--- 