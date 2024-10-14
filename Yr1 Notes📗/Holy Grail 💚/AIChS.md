# AI Cheat Sheet
---
> [!info]+ Cheat Sheet Details
> Includes information about (genus:: Cheat Sheet), link to CS module and it's correspondent attribute tag
> *Module Tag :* (ModCode :: CM12001) 
> *Link :* [[Artificial Intelligence 1]]
> *Cheat Sheet tag :* [[Grail 🩷]]

---

1. **MDP**
	- $a)$ Components - 
		- States $\{s_0,s_1,...,s_n\}$
		- Actions for each $s$ $\{s_0,s_1,...,s_n\}$
		- Rewards
		- Probabilities
    - $b)$ Bellman Equations 
	    - $V^π(s)=E_{a∼π}(s)​[R(s,a)+γ\sum_{s^′}{​P(s^′∣s,a)V^π(s′)}$
	    - $V$ of $s=$ $Immediate \space Reward + Future \space Reward$
    $c)$ Value Iteration - 
    $d)$ Policy Iteration - 
    
2. **State-space search** 
    $a)$ Heuristic Search $= Approximation$ 
    $b)$ A* Algorithm  $h(n) = g(n) + h'(n)$
    $c)$ Constraint Satisfaction Problems - $sudoku$

3. **Bayes theorem** 
    $a)$ $P(x|y) =\frac{P(y \wedge x)}{P(y)}= \frac{P(y|x)P(x)}{P(y)}$
	$b)$ $P(c|n_1,n_2,n_3) = \frac{P(n_1,n_2,n_3|c)P(c)}{P(n_1,n_2,n_3)}$
		When in Bayes net, $Denom$ of $frac$ commonality $\therefore$ can be ignored
	
4.  **Algorithms**
    $i.$ K-nearest neighbours  
		Create n points, take k nearest to each point, avg, replot points. Recurse - take k nearest & plot till no more changes 
    $ii.$ Naive Bayes  
	    Naive as assumes all features Independent. Uses Bayes theorem
    iii. Machine Learning 
     Forward go brr back propog go brrrr
    $1)$ Supervised Learning - Training **ALREADY** classified / labeled e.g cats & dogs 
    $2)$ Unsupervised Learning  - Training **NOT** classified e.g weight & height
    $4)$ Overfitting and Underfitting  
	    Too much fitting for data = **bad** = Too little fitting
		**==BUT==** ***Simple solulu is normally best Solulu***

5. **Heuristics** 
    $a)$ All **Consistent** are **Admissible**, ==not all== Admis are Consistent 
    $b)$ **Admissible** -  Never overestimates cost $H(s) \geq h(s)$
    $c)$ **Consistent** -   $h(s) \leq c + h(s')$

    
6. **Social, legal, and ethical implications of AI** 
	$a)$ Privacy Concerns  
    $b)$ Bias and Fairness  
    $c)$ Accountability  
    $d)$ Transparency  
    $e)$ Impact on Employment
    
7. **Laws associated with AI use** 
	$a)$ Data Protection Regulations  GDPR
    $b)$ AI-specific Legislation  
    $c)$ Intellectual Property  
    $d)$ Liability Issues  
    $e)$ International Frameworks

---