
a human sitting down (but missing an arm and leg)
```tikz
\usepackage{tikz-cd}
\begin{document}
	\begin{tikzcd}
	~ & ~ & * \ar [r]& * \ar [l] \ar[r]& * \ar [l] ~&~&\\
	~ & ~ & * \ar [u]& ~ & * \ar [u] ~ & ~ &\\
	~ & ~ & * \ar [r] \ar [u]& * \ar [l] \ar[r]& * \ar [l] \ar [u] ~ & ~&\\
	~ & ~ & * \ar [ld] \ar[u] \\~ & ~ &* \ar [rd] \ar[u]~ & ~ &\\
	~ & ~ & ~ & ~ &~ & ~ & ~&\\
	
	\end{tikzcd}
\end{document}
```
In this human, there are immune cells. Viral particles, i.e. HIV, recognizes specific proteins to which it attaches. It inserts a viral particle to the cell. HIV (human immunodeficiency virus) is a virus that attacks the body's immune system. If HIV is not treated, it can lead to AIDS (acquired immunodeficiency syndrome). It has transcriptase and integrase proteins which convert RNA to DNA and and translate production into new viral proteins. AIDS causes a drop in helper T-cell counts over time, leaving patients susceptible to secondary infections. \
### Immune system
* Innate immune system (many kinds of cells)
* Adaptive immune system
	* B cells (B lymphocytes)
	* Cytotoxic T cells (cytotoxic T lymphocytes)
	* Helper T cells (helper T lymphocytes)

## HIV

#population: individuals from the same strain living inside a single patient
#allele: a genetic variant
* Population in blood is ~300 million virions
* Daily turnover: ~100 million new virions 
	* both numbers vary by patient and stage of infection

### Four forces that can change allele frequencies in populations
* Mutation
	* typically, a mistake is made when copying genetic materials.
	* HIV has a high mutation rate, $10^{-5}$ mutations per nucleotide
* Genetic drift
	* Multiple generations of genetic drift relies on chance. After n generations, some alleles get lost while others dominate. Or they could stay in any proportion.
	* drift removes variation
* natural selection  
	* the differential survival and/or reproduction of individuals in a population due to differences in their physical characteristics
* migration
	* Movement from one population to another, then reproduce in the second.

#heterozygosity: Measure of genetic variation in a population. The probability two alleles sampled randomly with replacement from the gene pool are different.  

see next: [[Molecular evolution]]
See further: [[A brief introduction to viruses]], 