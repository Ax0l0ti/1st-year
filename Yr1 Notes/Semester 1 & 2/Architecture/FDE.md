# Fetch Decode Execute Cycle
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :* DD-MM-YYYY21-11-2023
> > *Module :* #CM12002
> > *Teacher*: #FabioNemetz 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> >  [[#Overview]]
> [[#Detailed method]]
> [[#Fetch]]
> [[#Decode]]
> [[#Execute]]
--- 


## How does a CPU Work? 

A CPU works by repeating through a cycle grouped into 3 main parts : Fetch, Decode & Execute. This is known as the Fetch Decode Execute Cycle, or simply the FDE Cycle.!

### Overview

As a general overview of the following Cycle, a CPU fetches an instruction and its parameters from memory. It then stores these before executing the instruction within the CPU and saving the resultant output. 

![AltText|200](https://lh7-eu.googleusercontent.com/PJDN0PFld_z5fyOsysxp8o2__W47AYmogT2oDsSxrhBmqqZjHRpyAWav3x06Lzh_mbG5Kci_WgbcdIoSv6Wh3P_2uyXd6YPokOKY5l7fzETzPD4rI1CLko7FVeoEepWMRfy_cOxKG41iFFOqJS1QdYk)

### Detailed method
#### Fetch

At the start of a new FDE Cycle, the computer will fetch the address from one of the Special Purpose Register (SPR) called the Program Counter (PC) and store the address into the Memory Address Register (MAR) before calling a read request via the control bus to fetch the MAR address’s data.

This retrieved data, which is transported by the data bus, is then stored in the Memory Data Register. This retrieved data is made up of 2 parts: an operand and opcode. 

  

##### Opcode (instruction)
- Operation code. Specifies instructions that can executed by a CPU/processor in machine code
##### Operand (data)
- Value for which the Opcode uses as a parameter for execution which can either be a defined value or a defined register

The contents of the MDR are then transported into the instruction register in preparation for decoding the instruction. As the final step, the program counter is incremented to the next address that will be executed to prepare for the next FDE Cycle.

  

#### Decode

  

By decoding the Instruction, this provides both the required function method and how many operands the CPU should fetch for the instruction’s opcode. This method is completed using a binary decoder commonly called the instruction decoder.

#### Execute

After the control unit calls the correspondent function for the opcode, the values of operands are passed to the CPU components for manipulation e.g operations like addition and subtraction.

---