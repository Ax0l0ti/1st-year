# Instructions
---
*Date :*  14-11-2023 
*Module :* #CM12002 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]]
> [[# ]]
> [[# ]]
> 
--- 
### Representing and Executing Instructions

Any instruction requires:
- The operation to be executed
- The operands upon which the operation is performed

>Expressive power is the breadth of ideas that can be represented and communicated.

An operand is coded as an address where the actual operand is located. For example, addition could be represented as `Add 10,12` meaning add data in address 10 and address 12. 
- Instructions occupy more than one byte of storage
- Typically variable number of bytes

The memory hierarchy
	![[Memory Hierachy.png| 400]]

### Registers and the CPU

- Registers consist of arrays of bits (usually more than one byte)
- The ALU contains registers to hold processed data (Accumulators/data registers)
- Control unit has registers for storing program information

###### One and a half address codes
![[One and a half address codes.png]]
- If we have more than one data register, then we need only 3 bits in the instruction set without greatly increasing the amount of store we need to hold the instructions. 

##### Zero address codes
- These are instructions with no arguments
- For example INC Rn (increment register 'n')
- The computer is stops when operation is carried out
 ![[Zero Address Codes.png]]

###### Two address codes
`Code style used in most modern computers. `
![[Two Address codes.png| 300]]


### Addresses and Sequencing instructions

###### Registers
`In control Unit`
- **Program Counter (PC)**
	- Holds the address of the next instruction 
- **Instruction register (IR)**
	- Holds the instruction currently being executed 
	`Used for accessing Memoroy`
- **Memory Address Registers (MAR)**
	- Holds the address that is being accessed
- **Memory Buffer (MB)**
	- Contents of that location while they are being written into or read from the store

![[Pasted image 20221114120135.png | 300]]

### Fetch Decode Execute cycles
- **Fetch Phase**: Bring the instructions from store to the instruction register
- **Execution Phase**: Decoding the instruction, accessing the operands and carrying out the operation

To carry out an instruction:
	- Instruction must be fetched from store to the control unit
	- Decoded to determine what operation is to be performed
	- The operands must be fetched from store to the ALU
	- The operation upon them is executed

**Fetch**
The contents of the Program Counter are loaded into the MAR. The content of the address in the MAR is loaded into the MBR. The contents of the MBR is passed along to the Instruction Register. The instruction is ready for decoding. 

**Execution**
MAR is incremented. Contents of the address in MAR is placed in the MBR. Contents of the MBR are placed in the data register. 

The program counter fetches the instruction from main memory and places into the Instruction Register.  Then the instruction is decoded, and the value is stored in the Accumulator. The program counter increments and the CPU fetches the next instruction.

Operand addressing modes
**Direct**: the value of the given address is used. 
**Indirect**: The operand is a location of store which contain not data but another address(where the true operand will be found)
**Immediate**: The given value is used itself. 


### CISC vs RISC

>**CISC**: Complex Instruction Set Computer
>**RISC**: Reduced Instruction Set Computer

#### Design Philosophies for Instruction Sets
- **CISC**
	- More Powerful Instructions
	- Less registers
	- Arithmetic Instructions also perform memory accesses
	- More complicated to decode instructions
-  **RISC**
	- Simple Instructions
	- Simple decoding of instructions
	- Arithmetic instructions only use registers
	- More registers


### Instruction Types
- Arithmetic Instructions $\to$ provide computational capabilities for processing numeric data 
- Logic (Boolean) Instructions 
- Control Instructions $\to$ are used to branch to a different set of instructions
- Movement of data into or out of register or memory locations. 
- I/O instructions

### Branching

###### Unconditional Branch (Jump)
>A branch instruction in which the branch is always taken is an unconditional branch. *Used as a loop. *
![[Pasted image 20221121100743.png | 300]]

- The execute phase of these operations take the operand address and transfers it to the PC. 
- The next operation then comes from the location addressed by the PC, in the normal way.

###### Conditional Branch
Being able to make a choice of whether to branch or not is conditional branching. 

Conditional branches allow the programmer to construct the programming such as: 
	• **Decisions**: if a condition is true do X, else do Y; 
	• **Loops**: do Z a fixed number of times; or do Z until a condition is true;

#### Subroutines

- The subroutine is called by branching to the starting location of the block. 
- When the instruction completes, the subroutine return to the point at which it was called.
- To accomplish this a [[Data Structures#Stacks |STACK]] data structure is used. 

The stack frame used when calling subroutines generally includes:
	- The return address
	- Argument variables passed on the stack
	- Local variables 
	- Saved copies of any registers modified by the subprogram that need to be restored
