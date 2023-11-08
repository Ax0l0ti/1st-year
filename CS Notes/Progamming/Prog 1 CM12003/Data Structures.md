# Data Structures
---
*Date :* {{date: DD-MM-YYYY }}
*Module :* #CM12003
*Teacher*:  #DrWillemHeijltjes 
*Resources :*

---
##### Contents: 
> [[#Stacks]]
> [[#Stacks in Recursion]]
> [[# ]]
> 
--- 


### Stacks
Stacks work on the Last In, First Out principle (LIFO).This means that the data that was added last (most recently) is the first one to be removed. 

Stacks is used in functions such as undo tasks, calling several functions in successions in a program or reverse polish notation
![300](https://cdn.programiz.com/sites/tutorial2program/files/stack.png)

A stack has three operations : 
	- Push – Adds item to the end of the stack
	- Pop - Removes item from the last index
	- Peek – Returns item in the last index of the stack

### Stacks in Recursion
A stack data structure is used in recursive algorithms to temporarily store the calling function’s return address and local variables.
![300](https://miro.medium.com/max/1400/1*C3LaaTtC6miYoIlhkX7zQQ.png)

The parameters and variables are stored “above” those that went before (push operation). This means that program pops the stack, it will be in the correct order.