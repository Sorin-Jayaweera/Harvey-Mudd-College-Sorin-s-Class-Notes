**Heterozygosity, alleles, and genetic variation

In lecture this week, we introduced heterozygosity as a measure of genetic variation within a population’s gene pool.  Here, we will discuss these topics some more. 


The gene pool is all of the collective genetic material within a population of organisms.  For example, all of the HIV viruses within an infected individual comprise a population; likewise, all of the alligator lizards in Claremont form a population.  In this course, we will normally focus on a single gene within the gene pool, and often a single position in one gene.  For example, we could focus on what nucleotide (base) occurs at position #42 in a particular gene.  Geneticists use the term alleles to refer to different versions of a gene (or even a position within a gene).  When we are talking about a single position in a DNA sequence, there are 4 possible bases (A, C, G and T), so we can say there are 4 possible alleles at that position.

  

We often want to quantify genetic variation in a gene pool.  One simple measure would be the number of different alleles present for a particular gene (or position within a gene, if we are zoomed in to that level).  A better measure would take into account the relative  abundance of each allele.  Consider the following table, which shows the number of each DNA base at one position:

  

|   |   |   |   |   |
|---|---|---|---|---|
||A|C|G|T|
|Position #42|50|40|60|50|

  

(The numbers are how many individuals in the population have that base at Position #42.)  In this example, the frequencies (proportions) of each allele are not equal, but they are similar, so there is substantial genetic diversity at this position.

  

Here’s another example, say from a different position:

  

|   |   |   |   |   |
|---|---|---|---|---|
||A|C|G|T|
|Position #1809|10|150|15|25|

  

Here, we also have 4 different alleles present, but in much more unequal proportions.  In terms of genetic variation, Position #42 is more diverse than Position #1809, as the majority of individuals have the C allele at position #1809, whereas there is no majority allele at position #42.  

  

Here’s one way to think of variation: If you chose two different alleles at random from this population, what is the probability that they would be different?  In one extreme case, suppose you only had one allele present; in this case, you would always choose two of the same allele, so the probability they would be different is zero.  This would represent a minimally diverse gene pool.  At the other extreme, each allele would be present in equal proportions; you would therefore have a pretty good chance of drawing a pair of different alleles.  

  

Formally, we can define heterozygosity as the probability of choosing a pair of alleles that are different:

  

Heterozygosity = 1 - pA2 - pC2 - pG2 - pT2     

  

Where pA = the frequency (proportion) of allele A, etc.

  

For the two examples above, this gives heterozygosity = 0.745 for Position #42 and heterozygosity = 0.41375 for Position #1809.  You might want to verify these numbers.

  

As we saw in lecture, the maximum value of heterozygosity for a 4-allele situation is 0.75.  In an alternate universe where there were 10 different bases in the genetic code, the maximum heterozygosity would be 0.9.  It makes sense that a greater number of possible alleles should give us a higher value of our measure of genetic variation.  

  

If you’ve studied genetics before, you may be wondering why we use the term  heterozygosity in this way, which seems very different from how you used heterozygous or heterozygote previously.  Here’s the connection: in a species that is diploid (possessing 2 copies of each chromosome), a heterozygous individual is someone who has two different alleles for a particular gene.  If you imagine a population that mates at random, then the expected proportion of heterozygous individuals = 1 minus the expected proportion of homozygous (same alleles) individuals.  (You probably used the term Hardy-Weinberg proportions in this context.)  The calculations are exactly the same as we used above.  However, you most likely only considered genes with two different alleles, and you probably used p and q for the allele frequencies.  

  

So, our use of heterozygosity to quantify genetic variation is exactly equivalent to the expected frequency of heterozygotes in a diploid randomly mating population.  Note that we can use heterozygosity as a concept and measure for any population, whether it is diploid or not.  Geneticists like to use heterozygosity as a convenient measure of genetic diversity, as it is a simple index that combines information about the number of different alleles present as well as how close they are to equal frequencies.