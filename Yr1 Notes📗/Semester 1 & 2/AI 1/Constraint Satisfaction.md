# Constraint Satisfaction ( CSPs )
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :* {{date: 27-11-2023 }}
> > *Module :* (ModCode :: CM12001)
> > *Teacher*: #BenRalph 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[# ]]  [[#ChatGPT notes]]
> [[# ]]
> [[# ]]
> 
--- 
### ChatGPT notes 

Prompt : tell me about Constraint Satisfaction for an advanced university. please make it in depth with simpler descriptions to help someone learn the topic. Please list key terms for this topic

Response : Constraint Satisfaction is a problem-solving paradigm used in artificial intelligence and computer science. It deals with problems where the solution must satisfy a set of constraints that define relationships between variables.

> [!example] Key terms
> 1. **Constraint:** A restriction or limitation on the possible values that a variable can take.
> 2. **Variable:** A placeholder for a value that can change during the problem-solving process.
> 3. **Domain:** The set of possible values that a variable can take.
> 4. **Constraint Satisfaction Problem (CSP):** A problem defined by a set of variables, their domains, and a set of constraints that specify the allowable combinations of values.

--- 

### Heuristic Algorithms for Constrain Satisfaction Problems

#### Solving CSPs 

A **state** is an assignment of values for all or some variables

| **Term**       | **Definition** | **Opposite** |
| ---------- | ---------- | -------- |
| **state**      |   an assignment of values within a problem       | N/A         |
| **complete**   |   all variables assigned       | partial         |
| **consistent** |      doesnt violate constraints      |    inconsistent      |
| **solution**   |       complete and consistent | not a solution        |
#### Types of searches

[[Uniformed search]]
[[Informed Search]]
[[Informed Search#Hill climbing algorithm|Hill Climbing]]
Local Search
Wave function collapse - uses suposition

---