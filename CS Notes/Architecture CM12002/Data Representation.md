# Data Representation
---
*Date :*  24-10-2023 
*Module :* #CM12002 
*Teacher*: [Fabio Nemetz](https://moodle.bath.ac.uk/user/profile.php?id=490)
*Resources :* [Decimal to IEEE 754 - YouTube](https://www.youtube.com/watch?v=8afbTaA-gOQ&ab_channel=AbishaliniSivaraman)

---
##### Contents: 
> [[#Numeration Systems]]
> [[#Conversion between numeration systems]]
> [[#Signed integers]]
> [[#Floating Point Binary]]
> [[#Using Mantissa and Exponent]]
--- 

Electronic computers are based on two-state devices(transistors and logic gates). This can be related to the binary system. 
A binary digit(0 or 1) is called a bit.

### Numeration Systems
All numeration systems are representational, i.e. a form of coding. 
Coding should be devised so that the system:
	•has few symbols that are easy to remember;
	•is unambiguous;
	•is economical in use (the higher the base more economical);
	•is a useful quantitative measure;
	•can be easily manipulated, e.g. to perform arithmetic.

Elements of the numeration system are that: 
- as many digit symbols as the base are needed;
- the decimal system’s base or radix of ten, the cardinal number of standards in the basic set, is denoted by ‘10’;
- place values increase from right to left in successive powers of the base (a positional system);
- addition is used to make up a number consisting of combinations of digits and multiplication is used to make up the number represented by a digit in a specific place;
- there is an agreed starting point (the ‘unit’ place); and
- a point is used to denote this place.

Some examples of numerations systems: 
	Decimal notation: 10 symbols (0-9)
	Octal notation: 8 symbols (0-7)
	Binary notation: 2 symbols(0 and 1)

### Conversion between numeration systems

###### ==Converting from octal to decimal==
- Take the most significant decimal digit and times by $8^{n-1}$ where $n$ is the number of digits. $n$ decrements by one each time. 
- Example: Convert $134_8$ to decimal. 
	$1 \times 8^2 + 3 \times 8^1 + 4 \times 8^0 = 64 + 24 + 4 = 92$ 

###### ==Converting from octal to binary==
- Get each digit from the ocatal and create that number with 4 2 1 table. Look image below, makes more sense. 
	![[Pasted image 20221107213208.png || 300]]

###### ==Converting from Hex to decimal==
- Take the decimal representation of the most significant bit and times by $16^{n-1}$ where $n$ is the number of digits. $n$ decrements by one each time. 
- Example: Convert $1FCB_{16}$ to decimal
	$1 \times 16^3 + 15 \times 16^2 + 12 \times 16^1 + 11 \times 16^0 = 8139$ 

###### ==Converting from Decimal to Hex ==
- One way is to first convert decimal to binary and then convert hex like A levels time. Probably Easier. 
- Second method is a follows: 
	- Divide the number by 16
	- Take the remainder and $\times 16$. This gives the decimal represntation of the Hex.
	- Take the integer result from division and repeat

	- Example: Convert $255_{10}$ to Hex
		$$\begin{array}{} \frac{255}{16} = 15.9374 \to 0.9375 \times 16 = 15 \to F \\ 
		\frac{15}{16} = 0.9375 \to 0.9375 \times 16 = 15 \to F \end{array}$$
		Hence the answer is $FF_{16}$. **IMPORTANT**: Always read from bottom to top. 

### Signed integers

###### Sign and Magnitude
- The first bit represent the sign of the integer (0 for positive, 1 for negative)
- The remaining n bits represent the magnitude 

|       **Advantages**           | **Disadvantages**                         |
| -------------------- | ------------------------------------- |
| Easy to read         | Two reprentations of zero             |
| Symmetric about zero | Only 255 values represented in a cell |
|                      | Arithmetic becomes complicated                                    |

###### One's Complement
- Positive numbers are represent by adding a leading 0 as before. 
- Negative integers (-n) are represented by swapping 1's and 0's in n. 
![[Pasted image 20221025095259.png]]
This method simplifies arithmetic but leaves us with two representation of zero(+0, -0). 

###### Two's Complement 
We represent negative numbers(-n) by swapping 0's and 1's in n like with One's complement and then adding 1. 
We can represent numbers two's complement by follwing the steps:
	- First write the bit pattern for the positive number
	- Swap the numbers after the first 1

### Scientific Notation
This is where Mantissa and Exponent is used to represent floating point numbers. 
Scientific notation is useful because: 
	- It is simple to generate
	- Compact representation
	- Accurate
Disadvantages of scientific notation:
	- Some numbers can't be represented exactly e.x. $\frac{1}{3}, \pi$ 
	- Rounding erros

Any number can be represented in terms of two quantities:
	- Signed Mantissa (m)
	- Signed Exponent (x)
$Number =\pm m \times R \pm x$ where $R$ is the radix of the system. (10 in decimal)
The number is normalised if $1 \le  |m| < R$  (except zero)

### Floating Point Binary
$Number = \pm m \times 2^{\pm x}$
![[Pasted image 20221031114449.png | 300]]

Floating numbers are stored using the IEEE Standard. There are two basic formats for IEEE:
	- Single Precision: 32 bits (4 bytes)
	- Dobule Precision: 64 bits(8 bytes)

#### Using Mantissa and Exponent 

###### ==Converting from IEEE 754single precision floating point number==
- Firstly take the sign | 0 $\to$ is positive and 1 $\to$ is negative |
- For single precision **EXPONENT** is 8 bits. Convert to decimal and subtract the BIAS(127)
- The rest is the **MANTISSA**. Then $1 + 2^{-n} + 2^{-n} ...$. (Adding 1 as it's in normalised form)
- Finally the **VALUE = MANTISSA**$\times$ $2^{EXPONENT}$

Example:
	![[Pasted image 20221101092345.png]]
	Sign: $0$ $\to$ meaning number is positive
	Exponent $\to$ $01111100 = 124 \to 124-127 = -3$. (Taking away BIAS)
	Mantissa: $\to 1 + 2^{-2} = 1.25$ 
	Value: $\to 1.25 \times 2^{-3} = 0.15625$

###### ==Converting from decimal to IEEE 754single precision floating point number==
- Firstly decide on the sign | 0 $\to$ is positive and 1 $\to$ is negative |
- Secondly the MANTISSA has two parts:
	- First is the whole number; convert to binary
	- Multiply the decimal parts by 2 and repeat until 0 or you notice a repetation. Take first digit i.e. 0 or 1 each time to turn it to binary
- Write the number in binary representation mirror the decimal point and stuff
- Normalise the value by moving the decimal point after the 1. Remove the 1 before the decimal which gives us the MANTISSA. 
- Count the number of spaces the decimal moved **(n)** and add the BIAS (127) to **n** and convert to binary. 
- Final result: Sign Exponent Mantissa
- Example:
	![[Pasted image 20221108163038.png |400]]
