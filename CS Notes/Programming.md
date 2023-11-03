# Programming and Languages
---
*Date :*  04-10-2023 
*Module :* #CM12003 
*Teacher*: [Zack Lyons](https://moodle.bath.ac.uk/user/profile.php?id=25337)
*Resources :*

---
##### Contents: 
> [[#What is programming]]
> [[#Levels of Languages]]
> [[#Advantages of High and Low level languages]]
> [[#Variables]]
> [[#Functions]]
> [[#Local and Global Variables]]
> [[#Types]]
> [[#Recursion]]
> [[#Stack Data Structure]]
> [[#Stacks in Recursion]]
> [[#Iteration]]

--- 

### What is programming?
Programming is the process of breaking a large, complex task up into smaller and smaller sub-tasks until eventually the sub-tasks are simple enough to be performed with a simple programmable instrucitons. eg. 
				- Get data from keyboard, file etc...
				- Perform basic arithemetic operations
				- Perform some action repeatedly

Programming languages can be categorised into High and Low level languages. Computers can only execute low-level languages. Programs written in high-level languages are translate (compiled or interpreted) to machine code.

In this module [[The C programming language|C]], [[Java]] and [[Python]] programming languages are used. 

### Levels of Languages
**High Level Languages**
	- They are made for people
	- They mostly have transparent constructs 
	- They have convinient syntax

**Low Level Languages**
	- Made for Computers
	- Specific to controlling basic operations on given computer design

###### Advantages of High and Low level languages
| High Level Languages                   | Low Level Languages        |
| -------------------------------------- | -------------------------- |
| Easier and faster to program           | Maximum execution speed    |
| Easier to read and correct             | Minimum memory consumption |
| Transfaerable between differnt devices |                            |

High-level programing languages can be spearated into two paradigms:
	**- Imperative Languages
	- Declarative Languages** -->  Tells the computer what to compute, e.g. mathematical expression. SQL, HTML, Haskell are declarative languages. 

**Prinicples of high level**
	- Variables
	- Conditions
	- Loops
	- Functions
	- Recursion
	- Object Orientation

**Data types:**
	- Booleans
	- Integers / floating-point numbers
	- Strings / Characters
	- Pointers (references to memory locations)

### Variables
**Variable** is mutable data type whose value can change. Immutable variables whose value cannot change.

Typical operations that can be applied to a variable are: 
	- Instantiate
	- Assign a type to a variable
	- Lookup ("Use") the value of a variable
	- Update
	- Deallocate ("remove") a variable

**Terminology**
- A standalone piece of code is a statement
- x = .... is an assignement
- (2+3) x (5+x) is an expression


### Functions
Functions can:
	- Take some arguments through passing it as a parameter
	- Manipulate them to produce a result or return a variable

Functions in most other programming languages can also do:
	· Update variables
	· Read from input and send to output
	· Raise an error
	· Interact with memory, devices, and other computers

A function can have any number (including zero) parameters and void type function gives no return value. .

Functions aim to:
	- Simplify code by group complex set of code behind a single command
	- Make a program smaller by removing repetitive code
	- Once a function has been written, we can call it multiple time in our code

[[The C programming language#^ae8b75 | Check functions in C for syntax]]

### Local and Global Variables

The scope of a variables starts where it is declared, it is bound to an enclosing block ({…})

Local Variables $\rightarrow$ A variable is declared in a block (Eg function) and has a local scope

Global Variables $\rightarrow$ A variable declared at top level is a global variable and has a global scope

### Types

Programming Languages in which types are **fixed at compile times** are called **statically typed languages.** Most statically typed languages enforce this by requiring you to declare all variables with their datatype before using them.

A programming language in which types are **discovered at execution** time are called **dynamically typed languages**. This is the type of variable is “figured out” when you first assign it.

[[The C programming language#^04e900 | Look at type Conversions In C]]

### Recursion

Recursive algorithm $\rightarrow$ function calls itself with smaller input values and returns the result for current input by carrying out basic operations on the returned values for the smaller input

A recursive function has:
- A base case that terminates the recursive function when the condition is met
- Recursive calls to the same function, but with the inputs decreasing in size or complexity (Known as Recursive Step)

### Iteration

Iteration is the process of marking out a block of statements within a computer program for a defined number or repetition or until a condition is met.

A WHILE loop is used in situations where we do not know how many times a loop needs to be executed beforehand or until we want a specific condition to be met.

A FOR loop is used where we already know the number of times a loop needs to be executed.

[[The C programming language#^f51657 |Follow the link to see syntax in C]]

 | Recursion                                                                                                           | Iteration                                                                                             |     |
 | ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | --- |
 | Recursion is when a function repeatedly calls itself with smaller inputs as the parameter                           | Iteration is when a set of instructions are repeatedly executed                                       |     |
 | Recursive function contains a set of instructions, a statement calling itself and a base condition                  | Iteration contains an initialisation, iteration, condition, and a set of instructions inside the loop |     |
 | Recursion is applied to method                                                                                      | Iteration is applied to a set of instructions                                                         |     |
 | Base case decides when the recursion terminates                                                                     | Value decides the termination of statement                                                            |     |
 | Large numbers of recursion lead to stack overflow.                                                                  | Infinite iteration consumes CPU cycles                                                                |     |
 | Recursion causes overhead of repeated function calling. This means execution of recursion is slower than iteration. | Iteration does not have function calling overhead. This means execution of iteration is faster        |     |
 | Recursion reduces size of code                                                                                      | Iteration makes the size of code larger                                                               |     |


### Arrays
Arrays are usually written inside square brackets [ ]. 

Each item in an array is called an element. 
Each element is referred to by its numerical index.


### Encapsulation
Encapsulation usually means wrapping a piece of code in a function. 

### Generalisation
Generalisation means taking something specific and making it more general. 




 



 



 









### Complex datatypes
Complex datatype is a dataype that is made of one or more other datatypes. e.g. Array

Complex datatypes are useful because: 
	- Collect together data in useful ways
	- Provide functions that operate in them

This combination of data representation and the functions that operate on these data representations are also known as Abstract Data Type.
### Pass by value / Pass by refrence
Pass by value is where the parameter contains a value; such as passing an integer direclty into a function. 
On the other hand, passing by refrence passes a refrences instead of the exact value. A refrence is a nickname or alias for another variable. 
### Object Oriented Programming
OOP allows for: 
- **Abstraction**: ability to igonore details of parts and focus attention on a higer level of the problem. 
- **Modularisation**: the process of dividing a whole into well-defined parts, which can be built and examined separately, and which interact in well-defined ways
- **Encapulation**: the idea that individual parts should be responsible for their own state