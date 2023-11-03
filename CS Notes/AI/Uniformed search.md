# Uniformed search
---
*Date :*  14-11-2023 
*Module :* #CM12001 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[# ]]
> [[# ]]
> [[# ]]
> 
--- 
>A search algorithm is called **Complete** if it is guranteed to find a solution. 
>It is called **Optimal** if it is guranteed to find an optimal solution. 

The efficiency of an algorithm is measured using the big-O notation. This notation usually considers:
	- **Time Complexity**: number of nodes generated during the search
	- **Space Complexity**: maximum number of nodes stored in memory

### Breadth First Search
In breadth-first search, we expand the shallowest node in the frontier. Shallow means that it is closest to the root of the tree. 
<iframe 
		border = 0
		width=500
		height = 300
		src="https://s3-eu-west-1.amazonaws.com/engage-video-uk-transcoded/processed/bd9c5268-e672-4a41-be46-e5509c360cba/9b09cf8e2fb50f41b66af6ede61612febb8ac6656d968f4e1cddc74a4a505b3b/1080p.mp4"></iframe>

Breadth-first search is *complete* assuming that there are a finite number of sets and it is also *optimal* if the path cost is non-decreasing function of node depth. For example: fixed costs. 

The Breadth-first search has a time complexity of $O(b^d)$. This is because the first layer of the tree has one node, the second will have b, the third will have $b^2$ and so on.
It has a space complexity of $O(b^d)$. This is because the final layer of the tree will have the most nodes in memeory. 

### Depth-first search
In depth-first search, we always expolore the deepest node in the frontier first; the node that was most recently added to the frontier. 
<iframe 
		border = 0
		width=500
		height = 300
		src="https://s3-eu-west-1.amazonaws.com/engage-video-uk-transcoded/processed/f11a737c-9db6-46fe-8e7e-1411e21bba3f/3c604cdf0e91a48a2d7f85f8ebc7706130ca70dafda4198a6b68effa9d12d0d4/1080p.mp4"></iframe>

Depth-first is *complete* assuming finate states however, it is *not optimal*. 

Depth-first has the time complexity of $O(b^m)$ which is similar or worse than the breadth-first search. However it has a lower space complexity of $O(bm)$. This is because the search never needs to store many nodes. A depth-first search does not need to keep track of a node once it has explored all children. 
