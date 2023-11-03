# Data Storage
---
*Date :*  25-10-2022 
*Module :* #CM10194 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#The Sotre]]
> [[#Cell Contents]]
> [[#Cell addresses]]
> [[#Types of Memory Access]]
> [[#Address Space]]
--- 

Bits are grouped in sequences called cells. A possible size for a cell is 8 bits and it is called a byte. Sequence of 16 bits is called a word; and 32 or 64 bits are called long words. 

###### The Sotre
The store consists of a collection of cells. Each cell is given an address for identification. A cell is the smallest addressabe unit of a store. 
![[Pasted image 20221025092255.png | 200]]

### Cell Attributes
###### Cell Contents
- The states of the bits of a cell make up its contents. 
- If the states of each two-state device, or bit, were called A and B, we could write the contents of a byte, for example, as:  AABABBAB

###### Cell addresses
- Each cell has a unique address that identifies it. 
- Addressses are numbered from 0 to (m-1) for a store with m cells.  
- It is impossible to tell what the cell content represents (data or instruction) by looking at them. 

###### Types of Memory Access
- Sequential access $\to$ time to access cell with a given address depends on the adress of the cell just accessed. 
- Random Access Memory (RAM) $\to$ time to access contents of each cell does not depend on its address. 
	- Main memory is usually DRAM. 
	- Cache memory is usually SRAM. 

###### Address Space
- Address space is a range of addresses associated with physical or virtual locations. (cells, I/O ports, IP addresses etc...)
- The same address may refere to different location in different spaces. 
- The length of the address determines(bounds) the size of the space: processors are often referred to in terms of the length of their address space. 

