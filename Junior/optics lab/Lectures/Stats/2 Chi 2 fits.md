We have an experiment with a theoretical true value $\mu$, but experiment spreads it out so that we have a value $\bar{y}$ that is spread around $\mu$. 

We showed that an unbiased estimate of $\mu$ is $\bar{y}= \frac{1}{N}\sum_{N}^{}y_{n}$
We also have an unbiased estimate of the standard deviation
$$
\begin{align}
s \sqrt[]{ \frac{1}{N-1} \sum_{N=1}^{N} (y_{n}-\bar{y})^{2}} 
\end{align}
$$
We conclude that
$\mu=\bar{y}\pm s_{\bar{y}}$, where $s_{\bar{y}}= \frac{s}{\sqrt[]{ N }}$. 


An interpretation of $\mu$ is that it is the value which makes it most likely that we got the measurement results $y_{n}$ that we did, so its 'fitting' a gaussian to our data.


**If we assume that $P(y)$ is normal (this does not hold for all): 
$$
\begin{align}
P(y) = \frac{1}{\sqrt[]{2\pi \sigma'^{2}} }e^{ -\frac{(y-\mu')^{2}}{2\sigma'^{2}}}
\end{align}
$$

We can evaluate the probability that out of $N$ trials, we got the distribution we found.
$P(y)$ is a probability density, so we have to look within a small interval $\Delta y$.
(Probability of getting from $y_{1}$ to $y_{1}+\Delta y$).

This is $(P(y_{1})\Delta y) (P(y)\Delta y)\dots (P(y_{n})\Delta y)$
$$
\begin{align}
\left( \frac{1}{\sqrt[]{2\pi \sigma'^{2}} } \right)^{N}e^{- \frac{1}{2\sigma'^{2} }\left[ \sum_{n=1}^{N} (y_{n}-\mu')^{2} \right]}
\end{align}
$$
Remember, $\mu'$ is the variable - $y_{n}$ is just a set of numbers we measured. 
What is the $\mu'$ that maximizes the probability of getting everything? Its the one which minimizes the sum (because $e^{\text{ negative stuff }}$)
$$
\begin{align}
\text{ let } \xi &  \equiv \sum_{n=1}^{N} (y_{n}-\mu')^{2} \\
\frac{ d \xi}{d \mu' }  & = \sum_{n=1}^{N} 2(y_{n}-\mu')(-1)=0 \\
 & \sum_{n=1}^{N} (y_{n}-\mu') = 0 \\
 & \sum_{n=1}^{N} y_{n} - N\mu' = 0 \\
\mu'  & = \frac{1}{N} \sum_{n=1}^{N} y_{n}
\end{align}
$$


If we $P(x)$ is not normal (i.e. constant), then median would be a better estimator. 

We can make a statement for our experiment that 
$y(x_{m})= \bar{y}_{m}+ S_{\bar{y_{m}}})$

## Fitting a function
We're given $f(x;a,b)$ where $a,b$ are free parameters. 

Lets guess $y=f(x)$, where $f(x)=ax+b$.
Assume that $\bar{y}_{m}$ is from a normal distribution, with a true mean $f(x_{m})$ and variance $s_{\bar{y}_{m}}^{2}$.

$\chi^{2}$ is the value that maximizes the probability that we would get our experimental values.
![[Pasted image 20260126104248.png]]
