# Adversarial Search
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :* 22-06-2024
> > *Module :* #CM12001 
> > *Teacher*: 
> > *Resources :* #Chatted

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Speed run]]
> [[#Minimax Algorithm]]
> [[#Alpha-Beta Pruning]]
> [[#Heuristic Evaluation]]
> [[#Game Trees]]
---
### Speed Run

1. Break down of topic
	$a)$ Minimax Algorithm - The minimax algorithm is a decision rule for minimizing the possible loss for a worst-case scenario
	$b)$ $\alpha$-$\beta$ Pruning - $\alpha$-$\beta$ pruning is a search algorithm that seeks to decrease the number of nodes evaluated by the minimax algorithm in its search tree
	$c)$ Heuristic Evaluation - Approximate Reward 
	$d)$ Game Trees - Game trees are tree structures that represent the possible moves in a game, showing sequences of moves from the initial state to terminal states
---

### Detailed Explanation

#### Minimax Algorithm
The minimax algorithm is a decision rule for minimizing the possible loss for a worst-case scenario. It is used in decision-making and game theory to find the optimal move for a player, assuming that the opponent is also playing optimally. The algorithm involves constructing a game tree, evaluating the terminal states, and propagating these values back up the tree to determine the best move. It is widely used in two-player games such as chess and tic-tac-toe.

#### Alpha-Beta Pruning
$\alpha$-$\beta$ pruning is a search algorithm that seeks to decrease the number of nodes evaluated by the minimax algorithm in its search tree. 
It achieves this by eliminating branches that cannot possibly influence the final decision, thus reducing the computational complexity. This optimization allows deeper exploration of the game tree within the same time constraints, making it an essential technique in game-playing AI.

**$\alpha$** is the best value that the **maximizer** currently can guarantee at that level or above.   
**$\beta$** is the best value that the **minimizer** currently can guarantee at that level or below.


**function** minimax(node, depth, isMaximizingPlayer, $\alpha$, $\beta$):
    **if** node is a leaf node :
        **return** value of the node
    **if** isMaximizingPlayer :
        bestVal = -INFINITY 
        **for each** child node :
            value = minimax(node, depth+1, false, $\alpha$, $\beta$)
            bestVal = max( bestVal, value) 
            $\alpha$ = max( $\alpha$, bestVal)
            **if** $\beta$ <= $\alpha$:
                **break**
        **return** bestVal
    **else** :
        bestVal = +INFINITY 
        **for each** child node :
            value = minimax(node, depth+1, true, $\alpha$, $\beta$)
            bestVal = min( bestVal, value) 
            $\beta$ = min( $\beta$, bestVal)
            **if** $\beta$ <= $\alpha$:
                **break**
        **return** bestVal



![[Alpha-Beta Pruning Example.png]]
#### Heuristic Evaluation
Heuristic evaluation in adversarial search involves estimating the value or score of a game position without having to search to the terminal nodes. Heuristics are typically domain-specific rules or functions that provide a quick and reasonably accurate assessment of a position's desirability. They are crucial in practical implementations of game-playing algorithms where exhaustive search is computationally infeasible.

> [!info] Heuristic Defintitions
$a)$ All **Consistent** are **Admissible**, ==not all== Admis are Consistent 
$b)$ **Admissible** -  Never overestimates cost $H(s) \geq h(s)$
$c)$ **Consistent** -   $h(s) \leq c + h(s')$

#### Game Trees
Game trees are tree structures that represent the possible moves in a game, showing sequences of moves from the initial state to terminal states. Each node represents a game position, and edges represent possible moves. Game trees are used in algorithms like minimax and $\alpha$-$\beta$ pruning to systematically explore potential future states and determine the best moves. They provide a framework for analyzing and implementing strategies in various combinatorial games.

---