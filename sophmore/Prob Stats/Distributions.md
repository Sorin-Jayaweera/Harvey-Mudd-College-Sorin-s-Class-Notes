Recall:

Probability density functions have the following properties:
* $f_{x}(x)\geq 0\text{ for all x }$
* $\int_{-\infty}^{\infty}f_{x}(x)dx=1$
* $\int_{a}^{b} f_{x}(x)dx=P(a\leq X\leq B)$

The cumulative distribution function for $f_{x}(x)$ is just
$$
\begin{align}
F(x)=\int_{-\infty}^{a} f_{x}(x)dx \\
\text{ and we can go backwards to find an interval } \\
P(a\leq x\leq b)=F_{x}(b)-F_{x}(a) \\
\end{align}
$$

##### _Definition_ Exponential distribution
is the probability distribution for the wait times between events of a Poisson process. If an average rate is $\lambda,$ then
$$
\begin{align}
f_{x}(x,\lambda)=\left\{ {\lambda e^{-\lambda x}\, x  \geq0, 0 x<0}  \right\}
\end{align}
$$
We can show quickly that this follows the properties of a pdf by integrating.
$$
\begin{align}
\int_{-\infty}^{0} f_{x}(x)dx + \int_{0}^{\infty} f_{x}(x)dx \\
0 + \int_{0}^{\infty} \lambda e^{-\lambda x} dx \\
= -e^{-\lambda x}\bigg|_{0}^{\infty} \\
=1  
\end{align}
$$


We can think of radioactive decay as a Poisson distribution ( the number of decays), and model the wait time between decays as an exponential distribution.

##### _Definition_ Normal Distributions
Often it seems like everything is normally distributed, as it comes up when making large numbers of measurement. 

A normal distribution is symmetric. It has pdf 
$$
\begin{align}
f_{x}(X) = \frac{1}{\sigma \sqrt{ 2\pi }e^{-1/2}}\left( e^{\frac{-1}{2}\left( \frac{x-\mu}{\sigma} \right)^{2}} \right)
\end{align}
$$
We give this the notation $N(\mu,\sigma)$.

The standard normal distribution has mean $\mu=0,$ and standard deviation $\sigma=1$.

