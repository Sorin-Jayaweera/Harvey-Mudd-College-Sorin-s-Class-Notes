
by the Harvey Mudd College Bio 46 course staff

Extra reading for the avid viewer:
## Overview
  

The goal of the neighbor-joining algorithm is to determine the phylogenetic relationships between a set of species. It takes as input a matrix representing the distances between those species, and it returns a tree representing their phylogenetic relationships. Often the distances in the matrix are genetic, representing the amount of difference between sequences taken from the species of interest.

  

We begin with a high level description corresponding to the illustration below. Say we are trying to build a tree for four species, W, X, Y and Z. We start (left pane below) with a distance matrix for those species. Based on criteria described below, we pick two nodes (ie species) to merge (X and Z in this case). Then we create a small tree consisting of these two nodes merged (this involves figuring out how long the branches to X and Z should be, which we describe below). Next we must update the distance matrix, treating this newly merged tree as a ‘species’ of its own. So now we have a distance matrix where we have added this newly merged node, and removed the two nodes that it was made from.

  

![](https://lh7-us.googleusercontent.com/NsTOAynbpcHK9uOV5vEzhNguv2VEfKRRBj2UY-LBZGvCgCN9a43LaJsDFbeR0yzkGDJmDXUYt3vKMhO1syFTXf6Uat-2D1CQ_NvOMggBqaYRzwaSdyCguQ-CfTe5qZKKxNKIsIwLeGsiUZyTO6UM33U)

  
We now enter the next iteration (2nd pane). We find another pair of nodes to merge (W and the previously merged X,Z node). We merge them (the resulting node at the bottom of the pane contains X, Z and W) update the matrix and go on to the next iteration. We proceed until the matrix is down to two entries. In the example illustrated above that happens in the 3rd pane. At that point we break out of our loop and merge the final two nodes yielding the solution tree.

We’ll now describe these steps in more detail.

## Picking nodes to merge: the neighbor-joining metric


Let’s first think about how we pick two nodes to merge in this process. You might think that a good way would be to pick the two with the smallest distance between them. However, it turns out this approach can be thrown off if the rate of sequence change is different in the lineages leading to different species. As a result, we use a somewhat more involved measure, called the neighbor-joining metric.
 

Consider an example with five species (A-E) and the following distance matrix:

![](https://lh7-us.googleusercontent.com/xnf97E6s_GfnA-EIKnmFgyyBzjrYCqh3A9EFxSnPFWQxlJ4d7mcahPlg-0Sv18IAm_OZPaPJ4wdvIzsdVzmdkyWZ2W4gCJKCRM_XZrx3ZCOTeG9lNkrDlr676j9GxmkZGoqkvh7O4TDr9eXGnELEKUE)



The value of the neighbor-joining metric between species A and B will be

  

$$
NJmetric (A,B) =Distance(A,B) -Separation(A) - Separation(B)

$$
  
where separation expresses how far a node is from all the rest. For example

  

Separation(A) =$$
\begin{align}
\frac{\text{ Sum of distances from A to every other nodeNumber of nodes }}{\text{ Number of nodes }-2} \\
\frac{8 + 11 + 15 +17 }{3}=17
\end{align}
$$
and

$$
\text{  Separation(B) }=\frac{\text{Sum ofdistances from B to every other nodeNumber of nodes }}{\text{ Number of nodes }-2} 
\frac{8 + 7 + 11 +13}{3}=13
$$

Thus in this case
$$
NJmetric (A,B) =8 -17 - 13= -22
$$

To determine which pair of nodes to merge, we calculate the neighbor-joining metric for all pairs of species, and pick the pair that minimizes this. In our five species example, we get the following values for all pairs:

![](https://lh7-us.googleusercontent.com/snXmgZk3oK-BeB4dIsLzLr-plwDNV6C-SkhkxWJnZ4qLkWhrhXZnSHLg1Pv4STPuJ31novbdHbeAbjFUO8KTCVvSJYi_5XJ5SfWJ8xn-CUE1v8BPY1IBF-ne12Z4NdlhwTBhnj3vH-pjQutil8tLnio)

  
The pairs A,B and C,D are tied for the minimum value. We can choose either one of these pairs to merge first.


## Calculating branch lengths in the merged node
 

Continuing with our five species example, let’s imagine that we’ve chosen to merge A and B. That means we’re going to construct a new node by combining A and B. In order to do that, we need to know how long the branch leading to A in that newly merged tree should be, and how long the branch leading to B should be.

Clearly these branch lengths should depend on the distance between A and B in our input matrix. But because the rate of substitution can vary between lineages, it is not enough to just divide the distance between A and B by 2. The approach the neighbor-joining algorithm takes is to factor in the separation of each node from all the rest. In general, if A is very separate from the other nodes, and B is not very separate, then we’d like to make branch A long, and branch B short. In the converse case, we would make B long and A short. We can achieve this with the following calculations, which make use of the separation metric described above.

  
Length of branch A =$$
Distance(A,B) + Separation(A) - Separation(B)2=8+17-132=6 
$$

  

Length of branch B =$$
Distance(A,B) + Separation(B) - Separation(A)2=8+13-172=2
$$

 Creating the newly merged node


Having picked two nodes to merge, and figured out how long their branch lengths should be, our  next job is to make a representation of this newly merged node. As discussed in class, we represent trees with a four-tuple format: (Node name, left tree, right tree, branch length). Using that format, our newly merged node combining A and B will look like this:

('anc', ('A', (), (), 6.0), ('B', (), (), 2.0), 0)


Node name here is ‘anc’ since this is an internal node. Left tree is the tip representation of A, ('A', (), (), 6.0). Remember that above we figured out that the branch leading to A should have length 6. Similarly right tree will be ('B', (), (), 2.0), since we determined the branch leading to B should have length 2. Finally, we put 0 in the branch length position for our newly merged node, since we have not yet figured out how long the branch leading to it should be. (This will be determined in a later iteration).

## Momentary aside: some details about our python implementation
  

Let’s pause for a moment to say something about how you’ll implement this in python. The function you will write in the homework takes two inputs. One is a node list. And the other is a distance matrix in the form of a dictionary.
 

The node list passed in as input is simply a list of tips. Continuing with the example we’ve been working on, it would look like this:

  
tc1L = [

    ('A',(),(),0),

    ('B',(),(),0),

    ('C',(),(),0),

    ('D',(),(),0),

    ('E',(),(),0)

  ]


This list contains a representation of each tip, A-E. For example ('A',(),(),0) represents the tip labelled A, using our standard tuple-tree format.

We will be representing the distance matrix as a dictionary. The keys of the dictionary are tuples representing pairs of nodes. For example, we need an entry to represent the distance between node E and node D. The key for this entry is a tuple, combining the tip E and the tip D: 
 

(('E',(),(),0),('D',(),(),0))


There is also a value associated with this key which represents the distance between E and D.

The entire dictionary for our example looks like this:

tc1D={

(('A',(),(),0),('B',(),(),0)):8,

(('B',(),(),0),('A',(),(),0)):8,

(('A',(),(),0),('C',(),(),0)):11,

(('C',(),(),0),('A',(),(),0)):11,

(('A',(),(),0),('D',(),(),0)):15,

(('D',(),(),0),('A',(),(),0)):15,

(('A',(),(),0),('E',(),(),0)):17,

(('E',(),(),0),('A',(),(),0)):17,

(('B',(),(),0),('C',(),(),0)):7,

(('C',(),(),0),('B',(),(),0)):7,

(('B',(),(),0),('D',(),(),0)):11,

(('D',(),(),0),('B',(),(),0)):11,

(('B',(),(),0),('E',(),(),0)):13,

(('E',(),(),0),('B',(),(),0)):13,

(('C',(),(),0),('D',(),(),0)):10,

(('D',(),(),0),('C',(),(),0)):10,

(('C',(),(),0),('E',(),(),0)):14,

(('E',(),(),0),('C',(),(),0)):14,

(('D',(),(),0),('E',(),(),0)):18,

(('E',(),(),0),('D',(),(),0)):18

}  

## Updating the distance dictionary 

Now let us  return to the algorithm. In our example case we’ve already picked two nodes to merge, calculated their branch lengths, and made a tree version of the merged node. Our next job is to update the distance dictionary. We need to determine the distance from our newly merged A,B node, to all the other nodes. As an example, let’s consider the distance from this new node to node C. We can illustrate that distance with the following diagram:
  

![](https://lh7-us.googleusercontent.com/TTySS3AM1s1nFkxdk7jhDZzMYzM8ecoXEdAPtq0tRZTKAIooXJRalmGWzTs7LJC39jnlwaZ8CWiMjnw3S-hWVPyBtZs0X2E5kJgABHvGU13hv8kHK5boR0Y1u62JGRXHHhLbkkYDlvv8NB_d3QQ5Zi0)

The dotted line represents the distance from the new A,B node to node C, and is the quantity we’d like to calculate. We can get it with the following formula:


![](https://lh7-us.googleusercontent.com/vt0I-Rix8GHqdsu-5YtDZYaQgVW_MumNNhK9AMDfcvLoCw-H9gIiYl248sDMi2JM82EZfqixxeH56LVi7I-02C55n3OKBhep0yiYIXX0cjJczilcRRpBunY6s4_bFVIJbbcp7CEo7_0Fy5-X8Hay4N4)

To update the distance dictionary, we apply this same approach to calculate the distance from the new node to every other node in the node list (except the two nodes being merged).

  
## Updating the list of nodes

The last thing that remains to be done is to add the newly constructed node to the node list and remove the two nodes that were merged to create it. At this point we’ve finished one iteration.

## Future iterations and termination


The algorithm then repeats this process in subsequent iterations. Each time two nodes are merged. The process continues until only two nodes remain in the node list. At that point we break out of the loop and merge those final two nodes (giving the branch between them a length corresponding to their entry in the distance dictionary).