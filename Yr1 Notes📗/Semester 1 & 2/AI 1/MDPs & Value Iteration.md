# title
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :* DD-MM-YYYY
> > *Module :* 
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Speed run]]
> [[#Value Iteration]]
> [[#Policy Iteration]]
> [[#Comparison and Use Cases]]

--- 
### Speed run 

1. Break down of topic 
	$a)$ -  Val It
		$i)$ 
	$b)$ - Policy It
		$i)$ optimal when policy improvement makes no change
	$c)$ - 
---
### Value Iteration

**Definition**: Value iteration is a method used in Markov Decision Processes (MDPs) to compute the optimal policy. It iteratively updates the value function for each state until it converges to the optimal value function. The optimal policy is then derived from this value function.

**Equation**: The Bellman equation is central to value iteration. The update rule for value iteration is:

$V_{k+1}(s) = \max_{a} \sum_{s'} P(s'|s,a) \left[ R(s,a,s') + \gamma V_k(s') \right]$

Where:

- $V_k(s)$ is the value function at iteration $k$ for state $s$.
- $P(s'|s,a)$ is the probability of transitioning to state $s'$ given state $s$ and action $a$.
- $R(s,a,s')$ is the reward received after transitioning from state $s$ to state $s'$ via action $a$.
- $\gamma$ is the discount factor (0 ≤ $\gamma$ < 1).

The algorithm iterates until $V_{k+1}(s)$ converges to $V^*(s)$, the optimal value function.

### Policy Iteration

**Definition**: Policy iteration is another method used in MDPs to find the optimal policy. It involves two main steps: policy evaluation and policy improvement. The algorithm iterates between these two steps until the policy converges to the optimal policy.

**Steps**:

1. **Policy Evaluation**: Calculate the value function $V^\pi(s)$ for a given policy $\pi$. This involves solving the following set of linear equations:

$V^\pi(s) = \sum_{s'} P(s'|s,\pi(s)) \left[ R(s,\pi(s),s') + \gamma V^\pi(s') \right]$

2. **Policy Improvement**: Improve the policy by making it greedy with respect to the current value function:

$\pi'(s) = \arg\max_{a} \sum_{s'} P(s'|s,a) \left[ R(s,a,s') + \gamma V^\pi(s') \right]$

The algorithm alternates between these two steps until the policy $\pi$ converges to the optimal policy $\pi^*$.

### Comparison and Use Cases

- **Value Iteration**: Often used when the state and action spaces are small to moderate. It is straightforward but can be computationally intensive due to the max operation over actions in each iteration.
    
- **Policy Iteration**: Typically used when the state and action spaces are larger. Although each iteration might involve solving a system of linear equations, it often converges in fewer iterations than value iteration.
    

These algorithms are fundamental in reinforcement learning and are used to solve problems where an agent needs to make a sequence of decisions to maximize some notion of cumulative reward.

---