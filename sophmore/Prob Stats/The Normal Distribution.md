For a random variable $X$, the $Z-score$ (also known as the standard score) tell sus how many standard deviations $X$ is above or below the mean.
$z=\frac{x-\mu}{\sigma}$
Z scores allow for comparisons between variables from different normal distributions.
An observation $x_{1}$ is said to be more unusual )or more of an outlier) than another observation $x_{2}$ if $z_{1}>z_{2}$. 


The standard deviation of a normal distribution is
$$
\begin{align}
\sqrt{ np(1-p) }
\end{align}
$$
and mean is $np$.

##### _Definition_: Percentile
The percentile of $a$is the percentage of outcomes from a distribution that are lower than $a$. I.e. $P(x<a)=\int_{-\infty}^{a}f(x)dx$ where $f(x)$ is the probability distribution.



Lets do a practice problem. 11.5% of the population smokes. 400 randomly selected people are surveyed and 42/400 are asked. What is the probability of seeing 42 or less?

The bad way of doing this is binomial:
$$
\begin{align}
P(\#\leq 42)=P(x=0)+P(x=1)+\dots+P(x=42) \\
=\sum_{i=0}^{42} 10.115^{i}*(1-0.115^{400-i})
\end{align}
$$
The better way: We can say that the mean is $400*0.115,\sigma=\sqrt{ 400*0.115*(1-0.115) }$

We can get the $z$ score as 
$$
\begin{align}
z=\frac{(42)-\mu}{\sigma} \\
\text{ so we have } \\
p(z\leq 0.063)=0.7357
\end{align}
$$
You can calculate the z score, then do normcdf(-99,z,0,1) since the z scores follow a normal distribution with $\mu=0 \, \sigma=1$.



