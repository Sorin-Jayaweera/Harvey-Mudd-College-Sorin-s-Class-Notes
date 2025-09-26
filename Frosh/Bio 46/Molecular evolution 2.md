![[Pasted image 20240131090203.png|300]]
Toxoplasma gondii is a parasite that is able to reproduce sexually in cats, and asexually outside of cats. They really want to get to cats, so they have evolved behaviors to make rats more friendly towards cats. 

Recall:
	DNA is typically represented from 5' to 3' bases,
	 ![[Pasted image 20240131091712.png|300]]
 **Main takeaways:**
 Substitution:  a point mutation where A $\leftrightarrow$G or something similar and becomes fixed in a population.
 #Purifying selection:  Any new mutation is not advantages and is less likely to be fixed. Slows the substitution rate
 #Positive selection: Any mutation is advantages, selection drives the mutation to fixation. Increases the substitution rate
 #enzyme: protein catalyst, if something went at the natural rate it isn't fast enough. for example, reverse transcriptase catalyzes the formation between a chain of nucleotides and a new nucleotide
 #active_site: The part of the enzyme that is involved with forming bonds (ie covalent). 3 dimensional shape that is in the right position of the active site that makes catalysis possible.
 #jukes_cantor_correction: we have to account for the actual number of substitutions that happens
#dNTP: any new nucleotide, dATP, dGTP, dCTP, dTTP, (A,G,C,T)
#AZT: stops the replication of RNA/DNA. It subs in for dTTP but doesn't form a new bond to continue the chain. Review further in [[Molecular evolution]]

## The HIV genome in context
![[Pasted image 20240131090806.png|300]]
We can see that E.coli is very densely packed for protein coding, whereas human chromosomes are very sparsely packed. This makes gene identification a lot harder.  


## Phylogenetic trees of hosts vs pathogens

H$_{uman}$IV and S$_{\text{imian}}$IV are both variants of HIV. How does the phylogenetic tree built off HIV and SIV compare to the phylogenetic tree between their hosts? (humans vs primates/simians)

## Phylogenetic reconstruction methods

If we assume that substitutions roughly accumulate proportional to time. We can compare the sequence alignment, and see that a small difference is because a substitution occurred. 
### constructing a distance matrix between sequences
We measure distances by looking for substitutions. They are a numerous change that happens, and are easier to use as a metric compared to deletions. 

However, we have to accommodate for the fact that multiple substitutions could happen at the same site. I.e., the same spot could be changed twice.
We use the #jukes_cantor model to correct for multiple hits.

Imagine following evolution on a single nucleotide position in a series of discrete time steps where only one substitution can happen at a time. The probability of having any change is given by $\alpha$. The probability that it stays the same without changing is $1-3\alpha$ 

We have to possibilities: n could stay the same, or something that is not n but it changes to n 

This means $P_{t+1} = P_{n}(t)(1-3\alpha) + (1-P_{n}(t)\alpha)$

We can say that $$\begin{align}
\Delta P_{n}(t) &= P_{n}(t+1)-P_{n}(t) \\
&= P_{n}(t)-3\alpha P_{n}(t)+\alpha-\alpha P_{n}(t)-P_{n}(t) \\
&= -4\alpha P_{n}(t)
\end{align}$$
This gives us
![[Pasted image 20240131092917.png]]

Over a long time period, we would expect the probability of j given j at t=0 = $\frac{1}{4}$
and over a long period, we would expect j given k at $t=0$ = $\frac{1}{4}$
and that overall the base frequencies would go to 1/4.
While the real world isn't as neat, this is a decent enough model for right now.

![[Pasted image 20240131094125.png|300]]

We can express I(t) in terms of $\alpha \text{ and }t$
as 
$$
\begin{align}
I(t)= \frac{1}{4}+\frac{3}{4}e^{ -8\alpha t }
\end{align}
$$
The expression for the probability two nucleotides are different (prev. equation for them being similar) is
$$
\begin{align}
p=1-I(t) = \frac{3}{4}+\frac{3}{4}e^{ -8\alpha t }
\end{align}
$$
* Probability of a substitution per site per unit time: 3α  
* Expected number of substitutions per site in one lineage: 3αt  
* Expected number of substitutions per site separating the two strains:  
$$\begin{align}
K &= 6\alpha t \\
&= -\frac{3}{4}\ln\left( 1-\frac{4}{3P} \right)
\end{align}$$
We can use this model to predict the differences within a site:
![[Pasted image 20240131094825.png]]
There are 6 replacements on the site, and we can find the probability of those substitutions. 
### Neighbor-joining algorithm to make a tree from distances
See next time!

See next: [[Phylogenetic reconstruction]]
See previous: [[Molecular evolution]]
