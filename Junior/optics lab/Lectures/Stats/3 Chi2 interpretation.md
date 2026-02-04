
Chi squared is the output of the fit parameters, and is "how many variances away" is each data point. 

PTE: the probability that the $\chi^{2}$ would be bigger than the one we got. We hope for $\text{ PTE (aka } P_{>}\text{) }=0.5$.

$$
\begin{align} 
\chi^{2}  & = \sum_{m=1}^{M} \left( \frac{\bar{y}_{m} - f^{fit}(x_{m} )}{S_{\bar{y}_{m} } } \right)\\
\left< \frac{\chi^{2}}{M-p} \right>  & =1 \\
\end{align}
$$
Where $M$ is the number of data points across the range (not multiple measurements of one data point), and $p$ is the number of degrees of freedom. 
We subtract $p$, because we can always force a $0$ for $p$ number of data points in the fit (i.e. a $\mathscr{P}_{}^{3}$ can be constructed to hit exactly where three points land). There are $M-p$ data points that aren't guaranteed. Reducing the $\chi^{2}$ actually smears the error around all data points, so there are no $0$ but the others are also less than $1$.


If $\chi^{2} \ll 1$
Either really lucky, error bars are way too large, or the errors across each data point in a series (not all one measurement point) are correlated. Errors not being random biases one way or another.

if $\chi^{2} \gg 1$
Either a really unlucky, really bad fit, or error bars are way too small/. 


How do we know when we were lucky/unlucky, or when we need to check experiment / fit?
* Number of degrees of freedom relative to number of data points
* $\chi^{2}$ is the sum of the squares of $M-p$ standard normal random variables  (mean 0, variance 1 because we subtracted the mean, and divide by the variance). 
* PTE is a guide: 
	* ![[Pasted image 20260128103330.png]]
	* We have a probability distribution for what $\chi^{2}$ we got given the number of degrees of freedom. ($M-k$) where $k$ is the number of data points. 
	* What is the probability that someone would get something bigger than my $\chi^{2}$ because of random error. 
	* 