# The C programming language
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :*  20-12-2023 
> > *Module :* #CM12003 
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Commenting]]
> [[#Data types in C]]
> [[#Conditionals]]
> [[#Arrays]]
> [[#Pointers]]
> [[# ]]
> 
--- 


###### Commenting
```C 
// Double slashes for a single line comment

/* The slash and star as 
shown are used for multi line comments */
```

Importance of commenting: 
	- to explain code
	- refresh your memory
	- Help others read your code
	- Re-use your code

``` C
#include <stdio.h>

// The "include" keyword is used to import code from another file. 

void main(){
	printf("Hello World");
}
```

###### Data types in C

- int integers 16-bit(minimum) 32-bit(typically)
- float floating point 32-bit(typically)
- double floating point 64-bit(typically)
- char characters 8-bit(typically)

Characters are written inside a '' single quotation.

C uses format specifiers; special codes in a string that determine how to print a data type. e.g. 
	- %c character, 
	- %d  decimal, 
	- %i integers, 
	- %f, %g floats

> These symbols are basically used like string concatenation in python. In the example below %d is replaced with the number 7


```C
/* Print an Integer */ 
# include < stdio .h > 
main () { 
	printf (" The number is %d \n" ,7) ; 
}
```

###### Variables
Variables in C refere to a location in memory of an appropriate pre-determined size which holds a value. If a variable is accessed before it is declared an error occurs. 

###### Functions in C

^ae8b75

Characters that can be used in C variable include:
	- UndersScore
	- Letters
	- Digits

A function in C is built by giving:
	- Return type
	- Function name
	- Parameters
	- Function body containing return statement
``` C
<return type> <function name>(<parameters){
	<function body>
	return <return values>
}
e.g 
int scramble( int eggs ) {

	return 69
}
```

C programs should have a main function with return type int. The return value of main indicates successful execution (0) or if an error occurred (any other number)

###### Boolean and Comparisons

Primitives Boolean Values are true and false (need to add “#include <stdbool.h>”)

We also have operators in C, this includes:
	- && (and)
	- || (or)
	- ! (not)

Comparison between numbers are also in C:
	- <
	- <=
	- >
	- >=
	- ==
	- != (not equal)

###### Conditionals

Conditionals in C are given by:
```C
if(<condition>){
	...
} else if(<condition>){
...
}else {
	...
}
```

There can be any number of else if block and the else block can be omitted.

###### Type Conversion
- Explicit (or Type Casting) done in C as:
	```C
	int n = 4;
	printf("%f",(double) n);
	```
- Implicit (or Type Coercion), as happens in C with arithmetic operators
	```C
	int n = 4;
	printf("%f",2.0/n);
	```

^04e900

###### Loops
While Loop
```C
int mult(int n, int by){
	int result = 0;
	while(by>0){
	result += n;
	by--;
}
	return result
}
```

For Loop
```c
int mult(int n, int by){
	int result = 0;
	for(int i=0; i<by; i++){
		result += n;
	}
	return result;
}
```
^f51657


### Arrays
```C
int myArray [7] // Declare array size i.e. number of elements
myArray[2] = 42; // assigning array
int n = myArray[2]; // acessing array element; 
```
The one liner for the code above can be done as: 
```C 
int myArray [2] = {12,24};
```

### Strings
Strings in C are stored as an one dimensional array of chars terminated by a null character \0

So a string "Hello" is actually a six char array (5 letters and a null character)

```C 
char greeting = "Hello";
//however this method means you can't assign values after
// The Code below is not valid
char greeting[];
greeting == "Hello"; // this is invalid
```

### Complex Datatypes
In C complex datatypes are constructed using 'Struct' keyword. 
```c
struct Contact { 
	char name [50]; 
	char phoneNumber [10]; 
};
```
### Pointers
Symbols * and & are associated with pointers. 

When * is found in a variable declaration, it denotes a pointer variable that points to a memory address Elsewhere, * “dereferences” a pointer – it gets the value being pointed to

![[Storing in Memory.png| 300]]

**&** gives the memory address (e.g. 0x6ffcd8) of a variable

```C
int n = 10;
printf("n = %d and address %p", n, &n);

is exactly the same as

int n = 10;
int* p = &n;
printf("n = %d and address %p", n, p);

// The code prints the following : 10 0x7fff6e890304
```
#### Pointer to a pointer 
``` C
int a; // Basic integer 
int *a; // Pointer to int
int **a; // pointer to address of pointer to int
```

### Pass by reference Vs Pass by Value 

| Pass by reference                                                                                                | Pass by Value - ==C language==                                       |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| assigning w a variable passes the refrerence address of that value                                               | assigning w a variable passes the actual value held in that variable |
| e.g<br>EVERYTHING is pass by value. but ==we can simulate PbR via Pointers==<br><br><br>\\\\ PbV but a can now be used for reference<br>int \*a = &n<br> | e.g<br><br>``` C<br>int n = 10;<br>```                               |
|                                                                                                                  |                                                                      |
#### You can add to pointers 

``` C
\\ pointers can simply be incrimented
int *p = &n;
p = p + 1;

```



![[DeepCopyViaPassByVal.png]]

---