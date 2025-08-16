
###### Detecting selection with the Ka/Ks ratio
by the Bio 46 course staff

  

### Types of natural selection

Evolution is the change in the frequency of alleles in a population over time. One of the forces that leads to evolution is natural selection: individuals with beneficial alleles are more likely to survive and reproduce, so those beneficial alleles tend to spread in the population, compared to other alleles. There are three different regimes for natural selection: no selection, positive selection, and purifying selection. Different regions of the genome may be under different types of selection at different times. 

  

No selection occurs when new mutations have the same fitness as any existing alleles in the population. In this case, changes in allele frequencies over generations may still occur due to random chance (genetic drift), but not due to selection.

  

Positive selection occurs when a new mutation has higher fitness than the existing allele or alleles in the population, which increases the chance that the new mutation will be fixed, compared to the case with no selection. Positive selection may occur, for example, when the environment changes, so that the population is no longer well adapted to its environment. For example, when a person with HIV undergoes a treatment, e.g. a multidrug cocktail, the population of HIV viruses is subjected to a new environment in which mutations that make the virus resistant to the drugs can be selected for. 

  

Purifying selection occurs when new mutations have lower fitness than the existing allele or alleles in the population, which decreases the chance that the new mutation will be fixed, compared to the case with no selection. Regions of the genome that are under purifying selection are evolutionarily conserved: that is, they tend to stay the same over many generations.

### Substitution rates

A substitution is a specific type of mutation (one that changes one nucleotide to another, e.g. an A to a T) that becomes fixed in the population. In the special case of no natural selection, the substitution rate (number of substitutions per site, per generation) is numerically equal to the mutation rate (number of mutations per site, per individual, per generation). This is because we expect N new mutations in the whole population (of size N) per site, per generation, each of which has a chance of 1Nto be fixed: s = N1N. At sites that are under positive selection, new mutations will have greater than a 1Nchance of becoming fixed, so they’ll have a higher substitution rate (compared to no selection). At sites under purifying selection, new mutations will have less than a 1Nchance of becoming fixed, so they’ll have a lower substitution rate (compared to sites with no selection).

  

We can compare genetic sequences to measure the substitution rate along the lineages leading to these sequences from the common ancestor. In this process, our first step is to align those sequences. This means we propose a set of insertions and/or deletions in each sequence, so that every pair of aligned nucleotides corresponds to the same nucleotide position in the common ancestor. In aligned sequences, gaps (produced by insertion or deletion mutations) are represented by the character “-”.  Once the two sequences have been aligned, we can count the number of positions at which they differ. We can then calculate a proportional difference, which is the number of sites where the nucleotides differ, out of all sites where there has been no deletion or insertion of DNA. For example, we could compare the aligned sequences:

  

ATT---GCT

ATCAATGCG

  

There are two nucleotide differences, in the third and last position, out of six positions with no gaps. This corresponds to a proportional difference of ⅓.

  

However, if we simply count the number of observable differences, we will underestimate the true substitution rate. This is because some substitutions may occur at the same site, and thus multiple substitutions would be indistinguishable from just one. To correct for this problem, we can apply the Jukes-Cantor correction, which estimates the number of substitutions per site that would have produced the observed proportional difference between a pair of sequences. The equation for the Jukes-Cantor correction is:

  

K=-3/4 ln(1-4/3 p)

  

When we compare two sequences that have diverged t generations ago, we expect the number of substitutions per site to be the substitution rate per generation, s, multiplied by the number of generations separating the two, 2t. 

  

### Synonymous and non-synonymous mutations

Although protein-coding genes make up only a small fraction of the genome, these are sections of the genome where we might be particularly interested in detecting positive or purifying selection. For example, the CCR5 gene in humans has a variant, the delta-32 allele, which confers resistance to HIV. The CCR5 gene codes for a protein whose function is to act as a receptor in our immune cells; the HIV virus uses that receptor to infect those immune cells. We might suspect that the delta-32 allele has become more frequent in certain populations because it provided protection against HIV infection. If this is true, then we should see evidence of positive selection in this gene. 

  

We can use the redundancy of the genetic code to differentiate mutations that could have a selective impact (either positive or negative) from those that we expect to be neutral. Protein-coding genes consist of a sequence of three-nucleotide codons, each of which corresponds to an amino acid, which are the building blocks of proteins. Because there are 64 possible three-nucleotide codons, but only 20 amino acids, there is substantial redundancy in the genetic code (for more on the genetic code, please review [Making Proteins](https://docs.google.com/document/d/1gTsC04Ka6Xt6WqAXrOEOzcmeWvDGeR8ckSz1GPqKBXU/edit?usp=sharing).) For example, there are four codons, all beginning with UC, which code for the amino acid serine. This means that a mutation in the third position of such a codon, e.g. a mutation of UCT to UCA, would not result in any change in the amino acid produced. Such mutations are known as synonymous mutations. Because they do not change the amino acid, they have no impact on the structure and function of the protein that is produced. For this reason, we can expect such mutations to be neutral (i.e. have no fitness impact). In contrast, any mutation which does change the amino acid is known as a nonsynonymous mutation. These mutations, because they change the makeup of the protein, may change its structure and function and thus have some kind of fitness impact, either positive or negative.

### The Ka/Ks ratio

Because synonymous mutations have no fitness implications, we expect the rate of synonymous substitutions (i.e. synonymous mutations that become fixed in the population) to be equal to the rate of synonymous mutations. In contrast, the rate of nonsynonymous substitutions could be higher than the rate of nonsynonymous mutations, if there has been positive selection, or lower than the mutation rate, if there has been purifying selection. This suggests a diagnostic tool: we can compare the number of nonsynonymous substitutions per site (Ka) to the number of synonymous substitutions per site (Ks). By comparing adjacent sites within the same region of the genome, on the same set of individuals, we ensure that the mutation rates , population size N, and number of generations since the last common ancestor t are all the same. Thus the ratio should isolate differences in the chance of fixation. If the Ka/Ks ratio is greater than 1, that implies that nonsynonymous substitutions have a higher rate of fixation than chance, suggesting positive selection. If the Ka/Ks ratio is less than 1, that implies that nonsynonymous substitutions have a lower rate of fixation than chance, suggesting purifying selection.

  

To actually calculate the synonymous and nonsynonymous substitution rates, we’ll look at a number of sequences and assume that we can choose one of them to represent the common ancestor of all the rest. (We typically won’t actually have the common ancestor, but we may have a sequence from an outgroup.) We can then compare each of the sequences to this presumed common ancestor to count the number of observable synonymous and non-synonymous changes. For example, let’s consider just a single codon in this group of eight sequences, where we assume that GTA (coding for valine) was the common ancestor:

  

![](https://lh7-us.googleusercontent.com/HIvumzHZpW9OhQUmP-rR8pIxdcc98f9nsAPqdKujZkQc02A4VN18Du95-8yZ4QRM4LxL6aB7DbejXy0WvYqbeO5O671c5SsTsHUuRD2Qc4Sd3j22REFh5uSTO2_MpMNMyhnI-cKAx2BxSmJ-UD177v0)

  

Note that three of these sequences have a nucleotide change resulting in a different amino acid (CTA and TTA code for leucine, while GCA codes for alanine), and two of them have a change resulting in the same amino acid (GTT and GTG code for valine). However, we can’t just compare these numbers directly, because changes in the first two sites will always produce a different amino acid, while changes in the third site will always produce the same amino acid. Thus there are twice as many possibilities to make a nonsynonymous change. To correct for this, we can calculate the average number of observable nonsynonymous changes, per nonsynonymous site (3/16) as well as the average number of observable synonymous changes, per synonymous site (2/8). We then apply the Jukes-Cantor correction to each of these, to estimate the actual number of nonsynonymous substitutions per site (Ka) and synonymous substitutions per site (Ks). Their ratio then tells us something about the type of selection that was acting in that region of the genome, over the time period covered since these sequences diverged.

  

KaKs=0.2160.304=0.711

  

Because this ratio is less than one, that suggests that amino-acid changing mutations were less likely to fix than mutations that did not change the amino acid. This is consistent with purifying selection, a situation in which the current amino acid is the one that confers the highest fitness.

**