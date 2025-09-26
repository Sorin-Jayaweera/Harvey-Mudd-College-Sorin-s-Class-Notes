We can treat the host that a pathogen is in as a state. We can draw a host and pathogen tree, then connect lines with pathogens and hosts they can infect. ![[Pasted image 20240205091440.png|300]]
We want to know the history that happened here. It could be that the pathogen existed in Host B and moved to A, or from A to B.![[Pasted image 20240205091510.png|600]]
We prefer the scenario on the left as more likely (" #parsimonious") because it requires the minimum number of events to happen.

![[Pasted image 20240205092916.png]]
Answer:
	![[Pasted image 20240205092941.png]]
	

At this current level we'll represent trees with the following:
(Node name, left tree, right tree, branch length)

Lets start with a distance matrix:
$$
\begin{bmatrix}
 & A & B & C & D \\
A & 0 & 6 & 6 & 6 \\
B & 6 & 0 & 4 & 4 \\
C & 6 & 4 & 0 & 2 \\
D & 6 & 4 & 2 & 0
\end{bmatrix}
$$
In the history of evolution between the species is reflected in the matrix. The tree that we want should have branch lengths that represent the matrix.
![[Pasted image 20240205093638.png|300]]
In the real world it isn't as neat, but we can still try to make it. For in depth on how to construct the tree algorithmically, see the [[Neighbor Joining Algorithm]]

![[Pasted image 20240205094630.png]]

On a high level, we start with a Node list that are all empty nodes.![[Pasted image 20240205094748.png|300]]



We search for nodes that are most closely related.
$$
\begin{bmatrix}
 & w & x & y & z \\
w & 0 & 9 & 4 & 9 \\
x & 9 & 0 & 9 & 2 \\
y & 4 & 9 & 0 & 9 \\
z & 9 & 2 & 9 & 0
\end{bmatrix}
$$
Here we can see the distance between Z and X is 2, so lets start with a tree X and Z. For now, we'll have a simple way of defining distance between them: splitting in half on the lowest nodes. We take X and Z out of the node list, and replace them with a branch that has 
('anc',("x",(),(),1.0),("z",(),(),1.0)). We now have to update the matrix to find the distance between this new "end". What is the distance between X and Y to the new node? We take the distance from x to y + distance from z to y - distance from x to z, then divide the result by two, and repeat that for every species.
![[Pasted image 20240205094704.png]]
![[Pasted image 20240205094853.png|500]]
And we continue this for many iterations. I leave it as an exercise to the reader to make the tree described by this matrix. 
Final output from the algorithm:
	![[Pasted image 20240205095023.png]]
	

Instead of the naive approach, we find a distance metric in a neater approach that takes in the distance between the two nodes - average distances to all other nodes for each of the two nodes, then find the minimum of that when choosing which nodes to start construction on. To find distance between those in construction, we follow a similar algorithm. 
![](https://lh7-us.googleusercontent.com/xnf97E6s_GfnA-EIKnmFgyyBzjrYCqh3A9EFxSnPFWQxlJ4d7mcahPlg-0Sv18IAm_OZPaPJ4wdvIzsdVzmdkyWZ2W4gCJKCRM_XZrx3ZCOTeG9lNkrDlr676j9GxmkZGoqkvh7O4TDr9eXGnELEKUE)

Separation(A) =
$$
\begin{align}
\text{ Sum of distances from A to every other nodeNumber of nodes } \\
\frac{8 + 11 + 15 +17 }{3}=17
\end{align}
$$
$$
NJmetric (A,B) =Distance(A,B) -Separation(A) - Separation(B)
$$


$$
\begin{align}

\text{ Length of branch A }= Distance(A,B) + Separation(A) - Separation(B)\\
2=8+17-132=6
\end{align}
$$

Length of branch B 
$$=
Distance(A,B) + Separation(B) - Separation(A)2=8+13-172=2
$$

for further reading with more in depth breakdown of the algorithm, see [[Neighbor Joining Algorithm]].

see previous [[Molecular evolution 2]]

