# Relational Algebra + SQL
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  12-12-2023 
> > *Module :* #CM12004DB 
> > *Teacher*: #BhagiPatel 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Basic Operators]]
> [[#Derive Operators]]
> [[#SQL commands]]
> 
--- 

#### Basic Operators
- Projection $(\pi)$
- Selection $(σ)$
- Cross Product $(x)$
- Union $(\cup)$
- Rename
- Set difference

#### Derive Operators
- Join
- Intersect $(\cap)$
- Division $( / )$

#### SQL commands
- DDL (Data definition)
	- CREATE
	- ALTER
	- DROP
	- TRUNCATE
	- RENAME
- DML (Data Manipulation)
	- SELECT
	- INSERT
	- UPDATE
	- DELETE
- DCL (Data Control)
	- GRANT
	- REVOKE
- TCL (Transaction Control)
	- COMMIT
	- ROLL BACK 
	- SAVE POINT

The below is defined for basic operators on a Student table as an example. 
![[Database Example.png]]
**Projection** works on columns. So in this case selecting all the name from Student would be projection. 

**Selection** works on rows. Selecting name,age from student with roll_no of 2 would be selection. 

**Cross product** is done between two tables. So our student table can link with lets say a course table. It is join operation on SQL. 

**Union** selects data from two diffent tables. So we can select name from student table and select name from employee table. It will display all names in those two tables. There are two conditions required for union:
	- Number of column must be same in both tables
	- Domain of every column must be the same

**Intersection** displays data where between two conditions both are true. For example selecting a student name from student table who is also an employee in the employee table. The conditions required for intersection is the same as for union.

---