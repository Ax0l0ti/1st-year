# Implementing Arithmetic
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  12-12-2023 
> > *Module :* (ModCode :: CM12002) 
> > *Teacher*: #FabioNemetz 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Adders]]
> [[#Subtractors]]
> [[#Shifts]]
> 
--- 

Combinational Boolean logic is used for arithmetic operations such as:
	- Addition
	- Subtraction
	- Multiplication
- on binary representations of 
	- Unsigned integers
	- Signed integers
	- floationg point numbers 

###### Adders
XOR can be used for addition operations. The carry is represented by the AND. The truth below is for a half adder (aka 1 bit adder). It takes 2 inputs and throws two outputs. It can only be used with 1 bit operations as no carry in input. 
![[Single bit Addition.png]]

The picture below shows the logic gate implementation of a full 1 bit adder. It has input A and B and the Carry In input. It gives two outputs, Sum and Carry out. 
![[Full adder Truth Table.png| 400]]
The boolean expression on the picture above is further simplified using XOR gates before being implemented as a circuit. 
![[Binary Arithmetic.png]]
![400](https://circuitdigest.com/sites/default/files/projectimage_tut/Full-Adder-Circuit.png)

However we may want to add more than one bits. Below is an example of a 4 bit adder; 4 full adders connected with carry out from one adder passed as carry in to the other. 
![[4 bit adder.png]]

### Subtractors
We can also create subtractors using the adders. Example of a 4 bit subtractor is shown below. The not gate converts a given binary into one's complement. Adding one to the one's complement with $C_0 = 1$ turns it into two complement's form. Hence we are adding one positive number with a negative number. 
![[Binary Subtractors.png]]

##### Arithmetic Overflow
When there is an overflow during arithmetic, we add another bit internally known as the guard bit. We add the guard bit to the most significant end of the integer representation. We copy the values on the guard bit from the most significant bit previously and perform the operation. 

Arithmetic overflow happens when the guard a bit in the result is different from the most significant bit of the 4-bit representation. 
![[Binary Addition Example.png]]

**Multiplication (Positive Integers)** can be done by adding repeatedly. However, this is not very efficient. So we can do long multiplication instead. 
Multiplying by powers of 2 is simply a case of shifting a bit pattern to the left. So each time power increases by we do a left shift. 

---
### Shifts

Shifts move bit patterns left or right by one or more places. 

There are three types of shift operation:
> [!abstract] Types of shift operations
> - Logical Shifts
> - Arithmetic shifts
> - Circular shifts

###### Logical Shifts
Logical **left shifts** move bits n-place to the left and corresponds to multiplication by $2^n$ on unsigned binary (overflow can occur). *Simply means left shift doubles the value each time*
![[LLS.png| 300]]
Logical right-shifts move bits n-places to the right and corresponds to division by $2^n$ (with rounding on unsigned binary). *Simply means right shift halves the value each time and remainders are ignored*
![[LRS.png| 300]]

###### Arithmetic Shifts
An arithmetic shift uses two’s complement so the left most bit is negative. 

With a **left arithmetic shift** the number is multiplied by 2 regardless of the sign. For a left shift an arithmetic shift = logical shift

With a **right arithmetic shift**, the sign is kept the same (left most bit) and then the numbers are shifted to the right. The number is divided by 2 and keeps the sign (fraction is lost).

###### Circular Shifts
Circular shifts bits are moved out of one end of a register are moved in at the opposite end of the register. 
For example rotate $11100101$ by 2 left shifts. This would result in $10010111$. All the bits move 2 to the left but instead of filling them with 0s we take the $11$ and place it in the other end.

---