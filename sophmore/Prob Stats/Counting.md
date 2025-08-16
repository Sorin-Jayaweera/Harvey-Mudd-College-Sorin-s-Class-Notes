Suppose that all outcomes of an event are equally likely.
Let $N=\text{ the number of outcomes in a sample space }$
Let $N(A)=\text{ the number of outcomes in event A }$

If we want to know the probability of A, $P(A)=\frac{N(A)}{N}$. This is the number of times that A happens out of the space of size $N$.

There are rules for counting to find these numbers

For Ordered collections, there is the Product Rule.
For Ordered subsets $S$ we have the Permutation Rule.
For Unorder subsets of S we have the Combination Rule.

## Product Rule
Suppose we have chosen an ordered collection of $k$ elements. To make this choice, say we have $n_{1}$ possible choices for the first element, $n_{3}$ possible choices for the second element, $\dots$, and $n_{k}$ possible choices for the $k$th element. Then the number of ways to pick $k$ such elements is 
$n_{1}\cdot n_{2}\cdot n_{3}\dots  n_{k}$

For example if we are choosing a 6 digit password using all numbers, then there are $10^{6}$ possible passwords that can be made, since any number can be used.

If each number could only happen once, its $10*9*8*7*6*5$, or $10!-(10-6)!$


## Permutations
Suppose there are $n$ objects in  a group, and we want to choose an ordered subset from the group of size $k$. Then the total number of orderings is $P_{k,n}=\frac{n!}{(n-k)!}$.

How many arrangements of the word math are there?
$n \choose k$ $= 4!$
Think of it as having 4 selections of letters for the first letter, then 3 selections for the next, and so on. For each of the 4 initial options, there are 3 secondary, etc, so $4*3*2*1$ options.


## Combinations
If the ordering doesn't matter, then there are $\begin{align}n \choose  k\end{align}$ ways of choosing the group, which is $\begin{align}\frac{n!}{k!(n-k)!}\end{align}$. This is commonly denoted $C_{k,n}$
$$
\begin{align}
k! \cdot C_{k,n} = P_{k,n}
\end{align}
$$

Lets try a problem.
A flush in a poker hand has all 5 cards of the same suite. What is the probability of being delt a flush from a randomly shuffled deck of cards?

There are 13 cards of the same suite, out of which 5 must be chosen. There are 4 suites total. There are 52 cards in a deck.

This gives us
4 * $13\choose 5$ total ways of drawing a flush out of $52 \choose 5$ ways of drawing a hand.


We could also reason through this by saying that there are $\frac{13}{52}$ cards for the first draw, $\frac{12}{51}$ for the second, etc, times four since there are 4 suites.