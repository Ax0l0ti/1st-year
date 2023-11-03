# Sequential Logic
---
*Date :*  13-12-2022 
*Module :* #CM10194 
*Teacher*: #FabioNemetz 
*Resources :*

---
##### Contents: 
> [[# ]]
> [[# ]]
> [[# ]]
> 
--- 

In a sequential system, the output of a logic gate can also be fed back so as to become the input to a gate 'earlier in the system'. This means that the output may depend not only on the current input but on previous inputs -- the system has state. 
 
### SR Latch (Set-Reset Latch)
Input combinations may result in any one of a number of stable or unstable states --- the system may be nondeterministic.
>**Nondeterministic:** even for the same input, it can exhibit different behaviors on different runs, as opposed to a deterministic algorithm.

A simple SR Latch implemented with NOR gates
![[Pasted image 20221213094042.png]]

SR latches are asynchronous (unlocked). Two separate gates can't switch simultaneously. There is a delay before a logic gate responds to an input. 

Below is a characteristic table for the SR latch above. It shows the Set (S) and Reset (R) inputs and the state of Q shown by $Q_n$. $Q_{n+1}$ shows the next state for Q. 
![[Pasted image 20230104204531.png | 300]]

###### Problems with simple SR Latches
- Asynchrous transitions
	- Circuts with several components, output states depend on the order in which changes to inputs occur
	- Solution: Use a clock input to enable/disable transition, yielding a gated latch or flip-flop. 
- Non-deterministic transitions associated with certain inputs
	- Solution: avoid states leading to such transistions by adding gates to control the inputs. 

### Flip-Flops
Flip-flops introduce a clock to latches: this synchronises state transitions across sequential logic circuits.
There are 3 types of flip-flops we'll look at:
	- SR
	- D
	- J-K

###### SR flip-flop (Clocked SR flip-flop or Gated SR latch)
A clock signal is added to the simple latch so the latch responds to inputs only when the clock signal is present, rather than at any time. 
So R and S inputs are passed to the NOR gates only during the clock pulse
![[Pasted image 20221213095430.png]]

###### D-type flip-flop
With SR flip-flop, R= 1, S=1 must be avoided. This can done by ensuring that the two inputs are always different. This can be done with a D-type flip-flop. 
by using and inverter, the non-clock inputs to the two AND gates are guaranteed to be opposite of each other. 
![[Pasted image 20221213095739.png | 300]]

•The D flip-flop is referred to as the data flip-flop because it is, in effect, storage for one bit of data. The output of the D flip-flop is always equal to the most recent value applied to the input. Hence, it remembers and produces the last input.

•It is also referred to as the delay flip-flop, because it delays a 0 or 1 applied to its input for a single clock pulse.

### J-K flip flops
This type of flip-flop makes use of the restricted combination (1,1). It is used to toggle, or change the output state, of the flip-flop.
![[Pasted image 20221213102154.png | 300]]
![[Pasted image 20221213102205.png | 300]]
The J-K flip-flop is a universal flip-flop: It can behave as an SR flip-flop or D flip-flop

### Using Flip-Flops
There are two types of registers:
	- Parallel registers (normal registers)
	- Shift registers (to implement shift operation)

###### Parallel Register
- Consists of 1-bit memories that can be read or written simultaneously
- Used to store data
- Clock to synchronise the simultaneous writing 
- Load: Control Signal (controls writing into the register)

###### Counters
- A register that can be incremented by 1
- After the maximum is achieved, next increment sets counter to 0
- Register of n flip-flops can count up to $2^n - 1$ 
- For example Program Counter
- They can be asynchronous or synchronous

###### Ripple Counter (asynchronous)
- The change that occurs to increment the counter starts at one end and "ripples" through to the ohter end. 
- Example: a 4-bit up counter using edge-triggered J-K flip flops. 
- J and K kept constant 1 (i.e. high)

###### Synchronous Counter
- Synchronous counters change all flip-flops of the counter at the same time