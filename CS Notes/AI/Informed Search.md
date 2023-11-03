 # Informed Search
---
*Date :*  21-11-2022 
*Module :* #CM10310 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]]
> [[# ]]
> [[# ]]
> 
--- 

# Greedy Search

We look at the smallest node after expanding the first node. The one with the smallest distance (cost) is chosen and explored. 

Greedy searches might not find us the optimal solution. So we need an **A star** search. 

A* search uses a heuristic to measure the estimated cost of each node, but also incorporates the total distance _actually_ travelled (from the initial state) when deciding the value of a node and, therefore, which one to expand next
![](https://moodle.bath.ac.uk/pluginfile.php/1915608/mod_page/content/20/Arad%20to%20Bucharest.png)
![](https://moodle.bath.ac.uk/pluginfile.php/1915608/mod_page/content/20/Arad%20to%20Bucharest.png)

![]https://moodle.bath.ac.uk/pluginfile.php/1915608/mod_page/content/20/Arad%20to%20Bucharest.png

<iframe 
		border = 0
		width=500
		height = 300
		src="https://s3-eu-west-1.amazonaws.com/engage-video-uk-transcoded/processed/828d4ce7-32aa-4dd6-a2de-472062379cd7/9847c5460ba4d8d1c532b9ba6a949c97698f4d8ee3c4f39483bb0fa8f14bc15d/1080p.mp4"></iframe>


### Properties of Heuristics

- It depends on the heuristics
- A heuristic is a function that takes nodes in a state space to numbers
- A heuristic is admissible if tit never overestimates the cost to reach the goal state
- With an admissible heuristic, an A* search will find the optimal solution
- A heuristic is consistent if it satisfies 

[picture](https://moodle.bath.ac.uk/pluginfile.php/1915608/mod_page/content/20/triangle%20inequality.png)

Hill climbing algorithm
- Start with a randomly generated state
- Generate all possible neighbours and take the one with the best value
- Repeat step 2 until none of the neighbours has a better value



