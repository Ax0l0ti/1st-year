# Uniprocessor Architectures
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  10-10-2023 
> > *Module :* (ModCode :: CM12002) 
> > *Teacher*: #FabioNemetz 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#The Von-Neuman Architectre]]
> [[#The Harvard Architecture]]
> [[#Caching]]
> [[#Registers]]
> [[#Parallel Architectures]]
> [[#Memory Architectures]]
--- 
Personal docs -
[Computer systems architectures ( CM12002 ) - Google Docs](https://docs.google.com/document/d/1EzEg2Ur3hNqMmzDv8KQfUXVzitG7Gmceo5SKTnZeyD8/edit#heading=h.4chf0znkme2v) 
### The Von-Neuman Architectre
- ==Arithemetic Logic Unit (ALU)== is where computational operations are carried out (math and logic). To carrout the operations we need:
	- An operation specification
	- Data or operands to operate upon

- ==Control Unit (CU)== is used to direct the flow of instructions. The main activities of the control unit are as follows:
	•Determine the operation to be performed
	•Select the correct operands and make them available when required
	•Perform the operation by supplying the correct control data to the ALU
	•Determine the next operation to be performed

Data and instructions are stored in a single store. This makes carrying out operations more flexible.  

A CPU is a combination of a control unit and the ALU. 

![[CPU Diagram.png]]  

###### Short Video on the Von Neumann Architecture
<iframe width="702" height="395" src="https://www.youtube.com/embed/5BpgAHBZgec" title="The Von Neumann Architecture" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
So these are the components of the von Neumann Architecture: 
	- Control Unit
	- Arithmetic Logic Unit (ALU)
	- Memory (Registers)
	- Connections (buses)
	- Input
	- Output

Characteristics of the Von Neumann Architecture: 
	- Discrete data
	- Storage of data in exact form
	- Instructions and data stored in same form and place
	- Processing capabilities e.g ALU
	- Control to enable automation
	- Communications via I/O devices

> In this course we'll study the componenet of the VonNeumann Architecture in more detail: 
> - ALU: circuits for addition and logical operations
> 
> - CU: 
> 	- instruction coding and execution, 
> 	- basic control operations(branching, subroutines), 
> 	- circuits for control(latches)
> - Store: 
> 	- digital representation of data
> 	- latches for storage
> 
> - I/O: different methods for controlling I/O (polling interrupts, direct memory access)

Questions: 
	- Describe the von Neumann Architecture
	- What are the main drawbacks of the von Neumann architecture?
	- How can they be overcome?

###### Von Neumann Bottleneck
The speed at which data and instructions can be retrieved from memory becomes a limit on which the speed of the processor can operate. The shared bus between the program memory and data memory leads to the Von Neumann bottleneck because program memory and data memory can not be accessed at the same time. 

**Solutions**:
	- Alternative architectures
	- Minimise use of main memory
		- Caching, 
		- Internal registers

### The Harvard Architecture 
The main idea behind Harvard architecture to store data and instruction separately. This means that the CPU can access instructions and data simultaneously. 
![[Data movement of CPU.png| 300]]

The Harvard architecture is useful:
	- In special-purpose devices like microcontrollers and signal processors (e.g., data from sensors) with instructions stored in ROM.
	- In sophisticated processors which can exploit the parallel fetching of code and data.
For example the Arduino Uno uses the ATmega328 microcontroller. 

Microcontrollers are designed for embedded applications. An embedded processor has a well defined task that it must perform reliably and efficiently and at minimal cost. **Harvard architecture** is a good match for embedded applications. 

**A software bug** is an error or fault in a computer program which causes it to produce incrorrect or unexpected results. 

Modifications made to the original Harvard Architecture: 
	- Provide a data pathway from the instruction store to the data store, so only one loading mechanism from store to CPU is required.
	- Have separate caching for code and data, but a single store, so that the processor can function in either Harvard or Von Neumann mode.

![[Von Neumann vs Harvard.png| 300]]


### Caching

Cache is a data store, which store data most often used by the CPU and is capable of more rapid access.
Cache is closer to the CPU and faster than RAM. 
![[CPU w other components.png| 400]]

#### Levels of Cache
- Cache Level 1 (**L1**)
	- closest to the processor
	- very fast, stores frequently used data by the CPU
- Cache Level 2 (**L2**):
	- Slower than L1, but faster than main memory
	- Larger than L1 cache
- Main memory
	- Larger and slower than cache
![[Simplified Computer.png| 200]]

**NOTE** : Increasing Cache size increases volume of storable data in cache at cost of **Longer fetch time** from retrieving individual addresses. ( This is why there is a L1 for high priority quick fetch and L2 for mid priority and quickish fetch required )
### Registers

Registers are rapid access data store on the CPU which stores values used in ongoing computations. It has the fastest possible access. 
![[Cache&RegisterAccess.png| 400]]


### Parallel Architectures

Parallelism is carrying out multiple operations simultaneously. 

==Von Neumann== machine is a ==uniprocessor== architecture whereas computers with multiple ALUs are known as multiprocessors. 

Multiprocessing is usually faster but much more difficult to understand, control and predict. So there are alternatives depending on whether each ALU has:
	- its own control unit (task level)
	- its own data storage (data level)

There are two possible control architectures for multiprocessors: 
	- Multiple instruction Streams --> Each ALU is controlled by a separate control unit ![[Multiple Instruction Streams.png| 200]]
	- Single instruction stream --> Single control unit issuing the same instruction to each ALU ![[Single Instruction Stream.png| 200]]
Independent of the control architecture the ALUs may either all operate on the same data stream or each operate on a different data stream. 

### Flynn's Taxonomy (Task level x Data level)
![[Flynn's Taxonomy.png]]
##### SISD: Single Instruction Single Data
uniprocessor architecture such as von Neumann or Harvard architecture ![[SISD diagrams.png]]

##### SIMD: Single Instruction Multiple Data 
Instructions are executed simultaneously. Same instruction from multiple memory locations. 
e.g. 
	- Supercomputer modelling (weather)
	- Signal Processing (sound, vision)
	- Graphics / audio applications
![[SIMD diagrams.png]]

##### MISD: Multiple Instruction Single Data
Different operations on the same data. Used for Falult Tolerant Computing. e.g for Space shuttle flight control computers. 
![[MISD diagrams.png]]

##### MIMD: Multiple Instruciton Multiple Data
Multiple processors functioniong asynchronously and independently. e.g multi-core processors. 
![[MIMD diagrams.png]]

### Memory Architectures
There are two possible memory architectures:  
- Shared memory  --> Each processor has access to the same memory
 ![[Shared Memory.png| 300]]

- Distributed memory --> Each processor has its own data store. 
 ![[Distributed Memory.png|  300]]


Shared memory:
	- leads to memory-to-CPU bottlenecks
	- Cache coherence becomes a problem 
	- because of the above they don't scale very well
	- ![[Shared Memory w Caches.png| 300]]
	
Distributed memory:
	- Easy to scale up for large numbers of parallel processors
	- Communication between processor is indirect, hence inefficient
	- Distributing and reassembling the data is inefficient
	- ![[Distributed Memory w Caches.png| 300]]

- **Virtual shared memory** $\rightarrow$ Distributed memory which "**seems**" shared to the CPUs. 
- **Non-uniform memory access (NUMA)** $\rightarrow$ shared memory which has parts which are faster for each CPU. 

### Limits of Parallelization

There is a limit of how much a process can be parellized -- e.g. if computation 'B' needs the output from computation 'A' as its input, then they cannot be computed in parallel. 

These constraints of data processing can be represented using series-parrallel graphs. 
![[CPU task execution.png| 300]]

###### Amdhal's Law
Amdhal's law states that for a given task, suppose a proportion $0 \le p \le 1$ can be parellised, but a proportion $s = 1-p$ is inherently sequential. So the maximum speedup obtainable by using **N** processors is: 
$$ \frac{1}{(1-p)+\frac{p}{N}}$$
Example: If 10% of a process is inherently serial, then running it on a quad-core proessor gives speed at most of what? 
$$\begin{array}{}
	\text{so from the question 90\% (0.9) is parallel and 10\%(0.1) is serial process}\\
	 \frac{1}{(1-p)+\frac{p}{N}} =  \frac{1}{(1-0.9)+\frac{0.9}{4}}\\
	 =3.08 \text{ times faster}
\end{array}
$$
After applying this formula in a case with infinite number of cores it is clear that after a certain point increase the number of cores has very little increase in speed. 
![[Amdahl's Law.png| 350]]

Example Question: 
	Calculate the maximum speed obtained when 50% of the process is parallel using 2 parallel processors. 
	$$\begin{array}{} s = 0.5, p = 0.5, N = 2 \\
	\frac{1}{(1-0.5) +\frac{0.5}{2}} \\
	= 1.33 \text{ times faster}
	\end{array} $$
---